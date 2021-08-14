---
description: Il codice di controllo configura un socket TCP per una latenza inferiore e operazioni più veloci sull'interfaccia di loopback.
ms.assetid: 4F7A6454-E3ED-4529-A531-B0640B0767EF
title: SIO_LOOPBACK_FAST_PATH codice di controllo
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 8650cd267d321569aca584e7195fb1bdb79c83a33d931e59e8db37521b8933a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740410"
---
# <a name="sio_loopback_fast_path-control-code"></a>SIO_LOOPBACK_FAST_PATH codice di controllo

## <a name="description"></a>Descrizione

Il codice di controllo **\_ SIO LOOPBACK \_ FAST \_ di** controllo PATH configura un socket TCP per una latenza inferiore e operazioni più veloci sull'interfaccia di loopback.

**Importante**  **L'istruzione \_ SIO LOOPBACK \_ FAST \_ PATH** è deprecata e non è consigliabile usare nel codice.

Per eseguire questa operazione, chiamare la [**funzione WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.

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
Usare **SIO \_ LOOPBACK \_ FAST \_ PATH** per questa operazione.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntatore al buffer di input.
Questo parametro contiene un puntatore a un valore booleano che indica se il socket deve essere configurato per le operazioni di loopback rapido.

### <a name="cbinbuffer"></a>cbInBuffer

Dimensione, in byte, del buffer di input.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntatore al buffer di output.
Questo parametro non viene usato per questa operazione.

### <a name="cboutbuffer"></a>cbOutBuffer

Dimensione, in byte, del buffer di output.
Questo parametro deve essere impostato su zero.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Puntatore a una variabile che riceve le dimensioni, in byte, dei dati archiviati nel buffer di output.

Se il buffer di output è troppo piccolo, la chiamata ha esito negativo, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [**WSAEINVAL**](windows-sockets-error-codes-2.md)e il parametro *lpcbBytesReturned* punta a un valore **DWORD** pari a zero.

Se *lpOverlapped* è **NULL,** il valore **DWORD** a cui punta il *parametro lpcbBytesReturned* restituito in una chiamata riuscita non può essere zero.

Se il *parametro lpOverlapped* non è **NULL** per i socket sovrapposti, le operazioni che non possono essere completate immediatamente verranno avviate e il completamento verrà indicato in un secondo momento.
Il **valore DWORD** a cui punta il *parametro lpcbBytesReturned* restituito può essere zero perché le dimensioni dei dati archiviati non possono essere determinate fino al completamento dell'operazione sovrapposta.
Lo stato di completamento finale può essere recuperato quando viene segnalato il metodo di completamento appropriato al termine dell'operazione.

### <a name="lpvoverlapped"></a>lpvOverlapped

Puntatore a una [**struttura WSAOVERLAPPED.**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

Se socket *s è* stato creato senza l'attributo sovrapposto, il *parametro lpOverlapped* viene ignorato.

Se *s è* stato aperto con l'attributo sovrapposto e il parametro *lpOverlapped* non è **NULL,** l'operazione viene eseguita come operazione sovrapposta (asincrona).
In questo caso, *il parametro lpOverlapped* deve puntare a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valida.

Per le operazioni sovrapposte, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce immediatamente e il metodo di completamento appropriato viene segnalato al termine dell'operazione.
In caso contrario, la funzione non restituisce finché l'operazione non è stata completata o non si verifica un errore.

### <a name="lpcompletionroutine"></a>lpCompletionRoutine

Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)

Puntatore alla routine di completamento chiamata quando l'operazione è stata completata (ignorata per i socket non sovrapposti).

### <a name="lpthreadid"></a>lpThreadId

Puntatore a una [**struttura WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) che deve essere utilizzata dal provider in una chiamata successiva a [**WPUQueueApc.**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)
Il provider deve archiviare la struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a cui si fa riferimento (non il puntatore allo stesso) fino a quando non viene restituita [**la funzione WPUQueueApc.**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)

**Nota**  Questo parametro si applica solo alla **funzione WSPIoctl.**

### <a name="lperrno"></a>lpErrno

Puntatore al codice di errore.

**Nota**  Questo parametro si applica solo alla **funzione WSPIoctl.**

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, la [**funzione WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce zero.

Se l'operazione ha esito negativo o è in sospeso, la [**funzione WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce **SOCKET \_ ERROR**.
Per ottenere informazioni estese sugli errori, chiamare [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).

| Codice di errore | Significato |
|------------|---------|
|**I/O WSA \_ \_ IN SOSPESO** | Operazione di I/O sovrapposta in corso. Questo valore viene restituito se un'operazione sovrapposta è stata avviata correttamente e il completamento verrà indicato in un secondo momento. |
| **OPERAZIONE WSA \_ \_ INTERROTTA** | L'operazione di I/O è stata interrotta a causa dell'uscita di un thread o di una richiesta dell'applicazione. Questo errore viene restituito se un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del **comando SIO \_ FLUSH IOCTL.** |
| **WSAEACCES** | È stato effettuato un tentativo di accedere a un socket in modo non consentito dalle autorizzazioni di accesso. Questo errore viene restituito in diverse condizioni per le prenotazioni di porte permanenti che includono quanto segue: l'utente non dispone dei privilegi amministrativi necessari nel computer locale o l'applicazione non è in esecuzione in una shell avanzata come amministratore predefinito ( `RunAs administrator` ). |
| **WSAEFAULT** | Il sistema ha rilevato un indirizzo puntatore non valido durante il tentativo di usare un argomento puntatore in una chiamata. Questo errore viene restituito dal parametro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *lpCompletionRoutine* non è completamente contenuto in una parte valida dello spazio indirizzi utente. |
| **WSAEINPROGRESS** | È in corso un'operazione di blocco. Questo errore viene restituito se la funzione viene richiamata quando è in corso un callback. |
| **WSAEINTR** | Un'operazione di blocco è stata interrotta da una chiamata a [**WSACancelBlockingCall.**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall) Questo errore viene restituito se un'operazione di blocco è stata interrotta. |
| **WSAEINVAL** | Argomento fornito non valido. Questo errore viene restituito se il *parametro dwIoControlCode* non è un comando valido o se un parametro di input specificato non è accettabile oppure il comando non è applicabile al tipo di socket specificato. |
| **WSAENETDOWN** | Rete inattiva rilevata durante l'operazione del socket. Questo errore viene restituito se il sottosistema di rete ha avuto esito negativo. |
| **Wsaenotsock** | È stata tentata un'operazione su un oggetto che non è un socket. Questo errore viene restituito se il descrittore *s* non è un socket. |
| **WSAEOPNOTSUPP** | L'operazione tentata non è supportata per il tipo di oggetto a cui si fa riferimento. Questo errore viene restituito se il comando IOCTL specificato non è supportato. Questo errore viene restituito anche se **\_ \_ l'FAST IOCTL \_ SIO LOOPBACK non** è supportato dal provider di trasporto. |

## <a name="remarks"></a>Commenti

Un'applicazione può usare **SIO \_ LOOPBACK \_ FAST \_ PATH** IOCTL per ridurre la latenza e migliorare le prestazioni delle operazioni di loopback in un socket TCP.
Questo IOCTL richiede che lo stack TCP/IP usi un percorso rapido speciale per le operazioni di loopback su questo socket.
**L'istruzione SIO \_ LOOPBACK \_ FAST \_ PATH** IOCTL può essere usata solo con socket TCP.
Questo IOCTL deve essere usato su entrambi i lati della sessione di loopback.
Il percorso rapido di loopback TCP è supportato tramite l'interfaccia di loopback IPv4 o IPv6.

Il socket che prevede di avviare la richiesta di connessione deve applicare questo IOCTL prima di effettuare la richiesta di connessione.
Il socket usato dalla funzione [**connect,**](/windows/desktop/api/winsock2/nf-winsock2-connect) [**ConnectEx,**](/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex) [**WSAConnect,**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnect) [**WSAConnectByList**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist)o [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamew) per avviare la connessione deve applicare questo IOCTL per usare il percorso rapido per le operazioni di loopback.

Il socket in ascolto della richiesta di connessione deve applicare questo IOCTL prima di accettare la connessione.
Il socket usato dalla funzione listen deve quindi applicare questo IOCTL in modo che tutti i socket accettati usino il percorso rapido per il loopback.
Tutti i socket restituiti dalla funzione listen e passati alla funzione [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/desktop/api/winsock/nf-winsock-acceptex)o [**WSAAccept**](/windows/desktop/api/winsock2/nf-winsock2-wsaaccept) verranno contrassegnati per l'uso del percorso rapido speciale per le operazioni di loopback.

Dopo che un'applicazione ha stabilito la connessione in un'interfaccia di loopback usando il percorso rapido, tutti i pacchetti per la durata della connessione devono usare il percorso rapido.

**L'applicazione di SIO \_ LOOPBACK FAST \_ \_ path** a un socket che verrà connesso a un percorso non di loopback non avrà alcun effetto.

Questa ottimizzazione del loopback TCP comporta pacchetti che passano attraverso il livello di trasporto (TL) anziché il loopback tradizionale attraverso il livello di rete.
Questa ottimizzazione migliora la latenza per i pacchetti di loopback.
Quando un'applicazione acconsente esplicitamente a un'impostazione a livello di connessione per usare il percorso rapido di loopback, tutti i pacchetti seguiranno il percorso di loopback.
Per le comunicazioni di loopback, la congestione e la perdita di pacchetti non sono previste.
La nozione di controllo della congestione e recapito affidabile in TCP non sarà necessaria.
Questo, tuttavia, non è vero per il controllo di flusso.
Senza il controllo di flusso, il mittente può sovraccaricare il buffer di ricezione, causando un comportamento di loopback TCP non corretto.
Il controllo di flusso nel percorso di loopback ottimizzato per TCP viene mantenuto inserendo le richieste di invio in una coda.
Quando il buffer di ricezione è pieno, lo stack TCP/IP garantisce che gli invii non saranno completati fino a quando la coda non viene inviata mantenendo il controllo di flusso.

Le connessioni tcp fast path loopback in presenza di un callout Windows Filtering Platform (WFP) per i dati di connessione devono adottare il percorso lento non ottimizzato per il loopback.
I filtri WFP impediranno quindi l'uso di questo nuovo percorso rapido di loopback.
Quando è abilitato un filtro PAM, il sistema userà il percorso lento anche se è stato impostato **LOOPBACK SIO \_ \_ FAST \_ PATH** IOCTL.
In questo modo si garantisce che le applicazioni in modalità utente siano in grado di garantire la funzionalità di sicurezza COMPLETA DI WINDOWS.

Per impostazione predefinita, **SIO \_ LOOPBACK \_ FAST \_ PATH** è disabilitato.

Solo un subset delle opzioni socket TCP/IP è supportato quando si usa **SIO \_ LOOPBACK \_ FAST \_ PATH** IOCTL per abilitare il percorso rapido di loopback in un socket.
L'elenco delle opzioni supportate include quanto segue:

* **IP \_ TTL**
* **IP \_ UNICAST \_ IF**
* **\_HOP UNICAST IPV6 \_**
* **IPV6 \_ UNICAST \_ IF**
* **IPV6 \_ V6ONLY**
* **ACCETTARE \_ QUINDI \_ L'ACCETTAZIONE CONDIZIONALE**
* **SO \_ EXCLUSIVEADDRUSE**
* **SCALABILITÀ \_ \_ DELLE PORTE**
* **SO \_ RCVBUF**
* **\_RIUTILIZZOADDR**
* **TCP \_ BSDENTENT**

## <a name="see-also"></a>Vedi anche

[**IPPROTO_IP socket di rete**](/windows/desktop/winsock/ipproto-ip-socket-options)

[**IPPROTO_IPV6 socket di rete**](/windows/desktop/winsock/ipproto-ipv6-socket-options)

[**IPPROTO_TCP socket di rete**](/windows/desktop/winsock/ipproto-tcp-socket-options)

[**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**SOL_SOCKET socket di rete**](/windows/desktop/winsock/sol-socket-socket-options)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**Wsaioctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
