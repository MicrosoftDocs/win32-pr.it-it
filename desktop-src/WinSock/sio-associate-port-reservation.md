---
description: Il codice di controllo associa un socket a una prenotazione di runtime o permanente per un blocco di TCP o UDP identificato dal token di prenotazione della porta.
ms.assetid: 4CBFB5F8-1FA1-44BA-9932-6F0329A465CB
title: Codice di controllo SIO_ASSOCIATE_PORT_RESERVATION
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 69af4f396fabd32f948d7e43cbf348aa34fb1a9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232791"
---
# <a name="sio_associate_port_reservation-control-code"></a>Codice di controllo SIO_ASSOCIATE_PORT_RESERVATION

## <a name="description"></a>Descrizione

Il codice di controllo della **\_ prenotazione della \_ porta \_ di associazione sio** associa un socket a una prenotazione di runtime o permanente per un blocco di TCP o UDP identificato dal token di prenotazione della porta.
Questo IOCTL deve essere emesso prima che il socket venga associato.
Se e quando il socket è associato, la porta assegnata verrà selezionata dalla prenotazione della porta identificata dal token specificato.
Se non è disponibile alcuna porta dalla prenotazione specificata, la chiamata della funzione [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) avrà esito negativo.

Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ASSOCIATE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RESERVATION_TOKEN
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ASSOCIATE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RESERVATION_TOKEN
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
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
Usare **la \_ \_ \_ prenotazione della porta di associazione sio** per questa operazione.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntatore al buffer di input.
Questo parametro contiene un puntatore a una struttura di [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) con il token per la prenotazione della porta TCP o UDP da associare al socket.

### <a name="cbinbuffer"></a>cbInBuffer

Dimensione, in byte, del buffer di input.
Questo parametro deve essere almeno pari alla dimensione della struttura [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) .

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntatore al buffer di output.
Questo parametro non è utilizzato per questa operazione.

### <a name="cboutbuffer"></a>cbOutBuffer

Dimensione, in byte, del buffer di output.
Questo parametro deve essere impostato su zero.

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

Puntatore a una struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) che deve essere usata dal provider in una chiamata successiva a [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).
Il provider deve archiviare la struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a cui si fa riferimento (non il puntatore alla stessa) finché non viene restituito il risultato della funzione [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) .

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
| **\_operazione WSA \_ interrotta** | L'operazione di I/O è stata interrotta a causa dell'uscita di un thread o di una richiesta dell'applicazione. Questo errore viene restituito se un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del comando **\_ IOCTL di scaricamento sio** . |
| **WSAEACCES** | È stato effettuato un tentativo di accesso a un socket in modo non consentito dalle autorizzazioni di accesso. Questo errore viene restituito in diverse condizioni per le prenotazioni di porte permanenti che includono quanto segue: l'utente non dispone dei privilegi amministrativi richiesti nel computer locale o l'applicazione non è in esecuzione in una shell avanzata come amministratore predefinito ( `RunAs administrator` ). |
| **WSAEFAULT** | Il sistema ha rilevato un indirizzo puntatore non valido durante il tentativo di usare un argomento puntatore in una chiamata. Questo errore viene restituito dal parametro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *il lpCompletionRoutine* non è interamente contenuto in una parte valida dello spazio degli indirizzi utente. |
| **WSAEINPROGRESS** | È in corso un'operazione di blocco. Questo errore viene restituito se la funzione viene richiamata quando è in corso un callback. |
| **WSAEINTR** | Un'operazione di blocco è stata interrotta da una chiamata a [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall). Questo errore viene restituito se un'operazione di blocco è stata interrotta. |
| **WSAEINVAL** | Argomento fornito non valido. Questo errore viene restituito se il parametro *dwIoControlCode* non è un comando valido o se un parametro di input specificato non è accettabile o se il comando non è applicabile al tipo di socket specificato. |
| **WSAENETDOWN** | Rete inattiva rilevata durante l'operazione del socket. Questo errore viene restituito se il sottosistema di rete non è riuscito. |
| **WSAENOTSOCK** | Si è tentato di eseguire un'operazione su un elemento che non è un socket. Questo errore viene restituito se il descrittore *s* non è un socket. |
| **ILWSAEOPNOTSUPP** | L'operazione tentata non è supportata per il tipo di oggetto a cui si fa riferimento. Questo errore viene restituito se il comando IOCTL specificato non è supportato. Questo errore viene restituito anche se il provider di trasporto IOCTL di **\_ prenotazione della \_ porta \_ di associazione sio** non è supportato dal provider di trasporto. Questo errore viene restituito anche quando un tentativo di usare l'IOCTL di **\_ prenotazione della \_ porta \_ di associazione sio** viene eseguito su un socket diverso da UDP o TCP. |

## <a name="remarks"></a>Commenti

Il IOCTL di **\_ prenotazione della \_ porta \_ di associazione sio** è supportato in Windows Vista e nelle versioni successive del sistema operativo.

Le applicazioni e i servizi che devono riservare le porte rientrano in due categorie.
La prima categoria include i componenti che richiedono una determinata porta come parte dell'operazione.
Tali componenti preferiscono in genere specificare la porta richiesta al momento dell'installazione, ad esempio in un manifesto dell'applicazione.
La seconda categoria include i componenti che richiedono qualsiasi porta o blocco di porte disponibile in fase di esecuzione.
Queste due categorie corrispondono a richieste di prenotazione di porta specifiche e con caratteri jolly.
Richieste di prenotazione specifiche possono essere permanenti o Runtime, mentre le richieste di prenotazione di porta con caratteri jolly sono supportate solo in fase di esecuzione.

Per associare una prenotazione di porta TCP o UDP a una prenotazione permanente o di runtime, viene utilizzata la prenotazione della **\_ porta di associazione \_ \_ sio** .

La funzione [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) o [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) offre la possibilità per un'applicazione o un servizio di riservare un blocco persistente di porte TCP o UDP.
Le prenotazioni di porte permanenti vengono registrate in un archivio permanente per il modulo TCP o UDP di Windows.
Si noti che il token per una determinata prenotazione di porta persistente può cambiare ogni volta che il sistema viene riavviato.

Una volta ottenuta una prenotazione di porta TCP o UDP persistente, un'applicazione può richiedere le assegnazioni delle porte dalla prenotazione della porta aprendo un socket TCP o UDP, quindi chiamando la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) specificando il IOCTL di **prenotazione della \_ porta di associazione \_ \_ sio** e passando il token di prenotazione prima di eseguire una chiamata alla funzione di [**Binding**](/windows/desktop/api/winsock/nf-winsock-bind) sul socket.

Il [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL può essere utilizzato per richiedere una prenotazione di runtime per un blocco di porte TCP o UDP.
Per le prenotazioni di porte di runtime, il pool di porte richiede che le prenotazioni vengano utilizzate dal processo sul cui socket è stata concessa la prenotazione.
Le prenotazioni di porte di runtime durano solo fino a quando la durata del socket in cui è stato chiamato il comando IOCTL [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) .
Al contrario, le prenotazioni di porte permanenti create utilizzando la funzione [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) o [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) possono essere utilizzate da qualsiasi processo con la possibilità di ottenere prenotazioni permanenti.

Una volta ottenuta una prenotazione della porta TCP o UDP di runtime, un'applicazione può richiedere le assegnazioni delle porte dalla prenotazione della porta aprendo un socket TCP o UDP, quindi chiamando la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) specificando il IOCTL di **prenotazione della \_ porta di associazione \_ \_ sio** e passando il token di prenotazione prima di emettere una chiamata alla funzione di [**Binding**](/windows/desktop/api/winsock/nf-winsock-bind) sul socket.

Se entrambi i parametri *lpOverlapped* e *il lpCompletionRoutine* sono null, il socket in questa funzione verrà considerato come un socket non sovrapposto.
Per un socket non sovrapposto, i parametri *lpOverlapped* e *il lpCompletionRoutine* vengono ignorati, ad eccezione del fatto che la funzione può essere bloccata se socket *s* è in modalità di blocco.
Se il socket *s* è in modalità non di blocco, questa funzione verrà comunque bloccata poiché questo particolare IOCTL non supporta la modalità non di blocco.

Per i socket sovrapposti, le operazioni che non possono essere completate immediatamente verranno avviate e il completamento verrà indicato in un secondo momento.

Qualsiasi IOCTL può bloccarsi per un periodo illimitato, a seconda dell'implementazione del provider di servizi.
Se l'applicazione non è in grado di tollerare il blocco in una chiamata di funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** , si consiglia di eseguire l'i/O sovrapposto per le IOCTL che sono particolarmente probabilmente bloccate.

La **\_ prenotazione della \_ porta \_ di associazione sio** può avere esito negativo con **WSAEINTR** o **WSA_OPERATION_ABORTED** nei casi seguenti:

* La richiesta viene annullata dal gestore di I/O.
* Il socket è chiuso.

Il IOCTL di **prenotazione della \_ porta di associazione \_ \_ sio** passato alla funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** per una prenotazione di porta permanente può essere usato solo in un'applicazione quando l'utente è connesso come membro del gruppo Administrators.
Se **sio \_ associa \_ la \_ prenotazione di porta** IOCTL viene utilizzata in un'applicazione quando l'utente non è un membro del gruppo Administrators, la chiamata di funzione avrà esito negativo e verrà restituito **WSAEACCES** .
L'uso della **prenotazione della \_ \_ porta di \_ associazione sio** può anche avere esito negativo a causa del controllo dell'account utente in Windows Vista e versioni successive.
Se un'applicazione che utilizza questo IOCTL con una prenotazione di porta persistente viene eseguita da un utente connesso come membro del gruppo Administrators diverso dall'amministratore predefinito, la chiamata avrà esito negativo a meno che l'applicazione non sia stata contrassegnata nel file manifesto con **requestedExecutionLevel** impostato su *requireAdministrator*.
Se l'applicazione non dispone di questo file manifesto, un utente connesso come membro del gruppo Administrators diverso dall'amministratore predefinito deve quindi eseguire l'applicazione in una shell avanzata come amministratore predefinito ( `RunAs administrator` ) affinché questa funzione abbia esito positivo.

## <a name="see-also"></a>Vedi anche

[**associare**](/windows/desktop/api/winsock/nf-winsock-bind)

[**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[**DeletePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[**DeletePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token)

[**LookupPersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[**LookupPersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md)

[**SIO_RELEASE_PORT_RESERVATION**](sio-release-port-reservation.md)

[presa](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
