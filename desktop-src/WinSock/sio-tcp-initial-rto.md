---
description: Codice di controllo che configura i parametri di timeout di ritrasmissione iniziale (RTO) in un socket.
ms.assetid: F5ABAE57-E0F0-4AEB-825C-B53AEE8210E7
title: SIO_TCP_INITIAL_RTO codice di controllo
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 63ebbfd0d8d56c03d62c7bba417d69e3ac1a576abfc8c72ac489117a7d8b74c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097481"
---
# <a name="sio_tcp_initial_rto-control-code"></a>SIO_TCP_INITIAL_RTO codice del controllo

## <a name="description"></a>Descrizione

Il **SIO_TCP_INITIAL_RTO** di controllo delle transazioni configura i parametri di timeout di ritrasmissione iniziale (RTO) in un socket.

Per eseguire questa operazione, chiamare [**la funzione WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INITIAL_RTO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a TCP_INITIAL_RTO_PARAMETERS structure
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
  SIO_TCP_INITIAL_RTO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a TCP_INITIAL_RTO_PARAMETERS structure
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
Usare **SIO_TCP_INITIAL_RTO** per questa operazione.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntatore al buffer di input.
Questo parametro contiene un puntatore [**al TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) associato al socket.

### <a name="cbinbuffer"></a>cbInBuffer

Dimensione, in byte, del buffer di input.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntatore al buffer di output.
Questo parametro non è usato per questa operazione.

### <a name="cboutbuffer"></a>cbOutBuffer

Dimensione, in byte, del buffer di output.
Questo parametro deve essere impostato su zero.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Puntatore a una variabile che riceve le dimensioni, in byte, dei dati archiviati nel buffer di output.

Se il buffer di output è troppo piccolo, la chiamata non riesce, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [**WSAEINVAL**](windows-sockets-error-codes-2.md)e il parametro *lpcbBytesReturned* punta a un valore **DWORD** pari a zero.

Se *lpOverlapped* è **NULL,** il valore **DWORD** a cui punta il *parametro lpcbBytesReturned* restituito in una chiamata riuscita non può essere zero.

Se *il parametro lpOverlapped* non è **NULL** per i socket sovrapposti, verranno avviate operazioni che non possono essere completate immediatamente e il completamento verrà indicato in un secondo momento.
Il **valore DWORD** a cui punta il *parametro lpcbBytesReturned* restituito può essere zero perché le dimensioni dei dati archiviati non possono essere determinate fino al completamento dell'operazione sovrapposta.
Lo stato di completamento finale può essere recuperato quando viene segnalato il metodo di completamento appropriato al completamento dell'operazione.

### <a name="lpvoverlapped"></a>lpvOverlapped

Puntatore a una [**struttura WSAOVERLAPPED.**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

Se i socket *sono* stati creati senza l'attributo sovrapposto, il *parametro lpOverlapped* viene ignorato.

Se *s è* stato aperto con l'attributo sovrapposto e il parametro *lpOverlapped* non è **NULL,** l'operazione viene eseguita come operazione sovrapposta (asincrona).
In questo caso, *il parametro lpOverlapped* deve puntare a una [**struttura WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valida.

Per le operazioni sovrapposte, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce immediatamente un risultato e il metodo di completamento appropriato viene segnalato quando l'operazione è stata completata.
In caso contrario, la funzione non restituisce un valore finché l'operazione non viene completata o non si verifica un errore.

### <a name="lpcompletionroutine"></a>lpCompletionRoutine

Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)

Puntatore alla routine di completamento chiamata quando l'operazione è stata completata (ignorata per i socket non sovrapposti).

### <a name="lpthreadid"></a>lpThreadId

Puntatore a una [**struttura WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) che deve essere utilizzata dal provider in una chiamata successiva a [**WPUQueueApc.**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)
Il provider deve archiviare la struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a cui si fa riferimento (non il puntatore allo stesso) fino al termine della [**funzione WPUQueueApc.**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)

**Nota**  Questo parametro si applica solo alla **funzione WSPIoctl.**

### <a name="lperrno"></a>lpErrno

Puntatore al codice di errore.

**Nota**  Questo parametro si applica solo alla **funzione WSPIoctl.**

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, la [**funzione WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce zero.

Se l'operazione non riesce o è in sospeso, la [**funzione WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce **SOCKET \_ ERROR**.
Per ottenere informazioni estese sull'errore, [**chiamare WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).

| Codice di errore | Significato |
|------------|---------|
| **I/O WSA \_ \_ IN SOSPESO** | È in corso un'operazione di I/O sovrapposta. Questo valore viene restituito se un'operazione sovrapposta è stata avviata correttamente e il completamento verrà indicato in un secondo momento. |
| **OPERAZIONE WSA \_ \_ INTERROTTA** | L'operazione di I/O è stata interrotta a causa dell'uscita di un thread o di una richiesta dell'applicazione. Questo errore viene restituito se un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del **comando SIO \_ FLUSH** IOCTL. |
| **WSAEACCES** | Si è tentato di accedere a un socket in un modo non consentito dalle relative autorizzazioni di accesso. Questo errore viene restituito in diverse condizioni che includono quanto segue: l'utente non dispone dei privilegi amministrativi necessari nel computer locale o l'applicazione non è in esecuzione in una shell avanzata come amministratore predefinito ( `RunAs administrator` ). |
| **WSAEFAULT** | Il sistema ha rilevato un indirizzo puntatore non valido nel tentativo di usare un argomento del puntatore in una chiamata. Questo errore viene restituito dal parametro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *lpCompletionRoutine* non completamente contenuto in una parte valida dello spazio degli indirizzi utente. |
| **WSAEINPROGRESS** | È in corso un'operazione di blocco. Questo errore viene restituito se la funzione viene richiamata quando è in corso un callback. |
| **WSAEINTR** | Un'operazione di blocco è stata interrotta da una chiamata a *WSACancelBlockingCall.* Questo errore viene restituito se un'operazione di blocco è stata interrotta. |
| **WSAEINVAL** | Argomento fornito non valido. Questo errore viene restituito se il *parametro dwIoControlCode* non è un comando valido o se un parametro di input specificato non è accettabile o se il comando non è applicabile al tipo di socket specificato. |
| **WSAENETDOWN** | Rete inattiva rilevata durante l'operazione del socket. Questo errore viene restituito se il sottosistema di rete ha avuto esito negativo. |
| **Wsaenotsock** | È stata tentata un'operazione su un elemento che non è un socket. Questo errore viene restituito se il descrittore s non è un socket. |
| **WSAEOPNOTSUPP** | L'operazione tentata non è supportata per il tipo di oggetto a cui si fa riferimento. Questo errore viene restituito se il comando IOCTL specificato non è supportato. Questo errore viene restituito anche se il **SIO_TCP_INITIAL_RTO** IOCTL non è supportato dal provider di trasporto. |

## <a name="remarks"></a>Commenti

Un'applicazione può usare **SIO_TCP_INITIAL_RTO** IOCTL per controllare le caratteristiche di ritrasmissione iniziali (SYN/SYN+ACK) di un socket TCP, se necessario.
Se si usa questa opzione, un'applicazione deve fornire valori appropriati prima di avviare un tentativo di connessione TCP sul socket.

Il [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) IOCTL consente a un'applicazione di configurare il timeout di ritrasmissione iniziale (SYN) usato dal socket.

Un puntatore a [**una struttura TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) passato nel parametro *lpvInBuffer* consente a un'applicazione di configurare il tempo di round trip iniziale (RTT) usato per calcolare il timeout di ritrasmissione.
L'applicazione può anche configurare il numero di ritrasmissioni che verranno tentate prima che il tentativo di connessione non riesca.

## <a name="see-also"></a>Vedi anche

[Socket](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**Wsaioctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
