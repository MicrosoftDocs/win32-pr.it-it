---
description: Il codice di controllo Configura un socket TCP per una latenza più bassa e operazioni più veloci sull'interfaccia di loopback.
ms.assetid: 4F7A6454-E3ED-4529-A531-B0640B0767EF
title: Codice di controllo SIO_LOOPBACK_FAST_PATH
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: f32cba8a081d2eb268a3e93a362ccec9bf414d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315780"
---
# <a name="sio_loopback_fast_path-control-code"></a>Codice di controllo SIO_LOOPBACK_FAST_PATH

## <a name="description"></a>Descrizione

Il codice di controllo del **\_ \_ \_ percorso rapido del loopback sio** configura un socket TCP per una latenza più bassa e operazioni più veloci sull'interfaccia di loopback.

**Importante**  Il **\_ \_ \_ percorso veloce del loopback sio** è deprecato e non è consigliabile usarlo nel codice.

Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_LOOPBACK_FAST_PATH,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a Boolean value
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_LOOPBACK_FAST_PATH,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a Boolean value
  (DWORD) cbInBuffer,           // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
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
USA **il \_ \_ \_ percorso veloce di loopback di sio** per questa operazione.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntatore al buffer di input.
Questo parametro contiene un puntatore a un valore booleano che indica se il socket deve essere configurato per le operazioni di loopback veloce.

### <a name="cbinbuffer"></a>cbInBuffer

Dimensione, in byte, del buffer di input.

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
| **ILWSAEOPNOTSUPP** | L'operazione tentata non è supportata per il tipo di oggetto a cui si fa riferimento. Questo errore viene restituito se il comando IOCTL specificato non è supportato. Questo errore viene restituito anche se l'IOCTL del **\_ \_ \_ percorso veloce del loopback sio** non è supportato dal provider di trasporto. |

## <a name="remarks"></a>Commenti

Un'applicazione può usare l'IOCTL del **\_ \_ \_ percorso rapido di loopback sio** per ridurre la latenza e migliorare le prestazioni delle operazioni di loopback su un socket TCP.
Questo IOCTL richiede che lo stack TCP/IP usi un percorso veloce speciale per le operazioni di loopback in questo socket.
Il **\_ \_ \_ percorso veloce del loopback sio** può essere usato solo con i socket TCP.
Questo IOCTL deve essere utilizzato su entrambi i lati della sessione di loopback.
Il percorso veloce di loopback TCP è supportato tramite l'interfaccia di loopback IPv4 o IPv6.

Il socket che prevede di avviare la richiesta di connessione deve applicare questo IOCTL prima di effettuare la richiesta di connessione.
Quindi, il socket usato dalla funzione [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist)o [**con WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamew) per avviare la connessione deve applicare questo IOCTL per usare il percorso rapido per le operazioni di loopback.

Il socket in ascolto della richiesta di connessione deve applicare questo IOCTL prima di accettare la connessione.
Quindi, il socket usato dalla funzione Listen deve applicare questo IOCTL, in modo che tutti i socket accettati usino il percorso rapido per il loopback.
Tutti i socket restituiti dalla funzione Listen e passati alla funzione [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/desktop/api/winsock/nf-winsock-acceptex)o [**WSAAccept**](/windows/desktop/api/winsock2/nf-winsock2-wsaaccept) verranno contrassegnati per l'utilizzo del percorso rapido speciale per le operazioni di loopback.

Una volta che un'applicazione stabilisce la connessione su un'interfaccia di loopback usando il percorso veloce, tutti i pacchetti per la durata della connessione devono usare il percorso veloce.

L'applicazione del **\_ \_ \_ percorso rapido di loopback sio** a un socket che verrà connesso a un percorso non di loopback non avrà alcun effetto.

Questa ottimizzazione del loopback TCP genera pacchetti che passano attraverso il livello di trasporto (TL) anziché il loopback tradizionale attraverso il livello di rete.
Questa ottimizzazione migliora la latenza per i pacchetti di loopback.
Quando un'applicazione opta per l'impostazione del livello di connessione per utilizzare il percorso veloce di loopback, tutti i pacchetti seguiranno il percorso di loopback.
Per le comunicazioni loopback, la congestione e la riduzione dei pacchetti non sono previsti.
Il concetto di controllo della congestione e recapito affidabile in TCP non sarà necessario.
Questo, tuttavia, non è vero per il controllo di flusso.
Senza il controllo del flusso, il mittente può sovraccaricare il buffer di ricezione, causando un comportamento errato del loopback TCP.
Il controllo di flusso nel percorso di loopback ottimizzato per TCP viene mantenuto inserendo richieste di invio in una coda.
Quando il buffer di ricezione è pieno, lo stack TCP/IP garantisce che le trasmissioni non verranno completate fino a quando la coda non verrà gestita con il controllo di flusso.

Le connessioni loopback con percorso veloce TCP in presenza di un callout della piattaforma filtro Windows per i dati di connessione devono prendere il percorso lento non ottimizzato per il loopback.
Pertanto, i filtri WFP impediscano l'utilizzo di questo nuovo percorso veloce di loopback.
Quando è abilitato un filtro WFP, il sistema utilizzerà il percorso lento anche se è stato impostato l'IOCTL del **\_ \_ \_ percorso veloce del loopback sio** .
Ciò garantisce che le applicazioni in modalità utente dispongano della funzionalità di sicurezza WFP completa.

Per impostazione predefinita, il **\_ \_ \_ percorso rapido di loopback sio** è disabilitato.

Solo un subset delle opzioni del socket TCP/IP è supportato quando viene utilizzato l'IOCTL del **\_ \_ \_ percorso veloce del loopback sio** per abilitare il percorso veloce di loopback in un socket.
L'elenco delle opzioni supportate include quanto segue:

* **\_TTL IP**
* **\_unicast IP \_ se**
* **\_Hop unicast \_ IPv6**
* **\_Unicast IPv6 \_ se**
* **\_V6ONLY IPv6**
* **\_accettazione condizionale \_**
* **\_EXCLUSIVEADDRUSE**
* **\_ \_ scalabilità delle porte**
* **\_RCVBUF**
* **\_REUSEADDR**
* **\_BSDURGENT TCP**

## <a name="see-also"></a>Vedi anche

[**Opzioni di IPPROTO_IP socket**](/windows/desktop/winsock/ipproto-ip-socket-options)

[**Opzioni di IPPROTO_IPV6 socket**](/windows/desktop/winsock/ipproto-ipv6-socket-options)

[**Opzioni di IPPROTO_TCP socket**](/windows/desktop/winsock/ipproto-tcp-socket-options)

[**presa**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**Opzioni di SOL_SOCKET Socket**](/windows/desktop/winsock/sol-socket-socket-options)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
