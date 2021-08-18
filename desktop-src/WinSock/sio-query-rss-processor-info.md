---
description: Il codice di controllo esegue una query sull'associazione tra un socket e un core del processore RSS e un nodo NUMA.
ms.assetid: DAF18C92-B479-474F-B438-0746CBA20653
title: SIO_QUERY_RSS_PROCESSOR_INFO codice di controllo
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 6c0f690555beb19f7d5d79a81e2cc900194f731c3acacb075ae12dc304debffd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740383"
---
# <a name="sio_query_rss_processor_info-control-code"></a>SIO_QUERY_RSS_PROCESSOR_INFO codice di controllo

## <a name="description"></a>Descrizione

Il **codice di controllo SIO QUERY RSS PROCESSOR \_ \_ \_ \_ INFO** esegue una query sull'associazione tra un socket e un core del processore RSS e un nodo NUMA.

Per eseguire questa operazione, chiamare la [**funzione WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_RSS_PROCESSOR_INFO, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_RSS_PROCESSOR_INFO, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
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
Usare **SIO \_ QUERY RSS PROCESSOR \_ \_ \_ INFO** per questa operazione.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntatore al buffer di input.
Questo parametro non viene usato per questa operazione.

### <a name="cbinbuffer"></a>cbInBuffer

Dimensione, in byte, del buffer di input.
Questo parametro non viene usato per questa operazione.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntatore al buffer di output.
Questo parametro deve puntare a una struttura [**\_ \_ AFFINITY PROCESSOR SOCKET**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) se i parametri *lpOverlapped* e *lpCompletionRoutine* sono **NULL.**

### <a name="cboutbuffer"></a>cbOutBuffer

Dimensione, in byte, del buffer di output.
Questo parametro deve avere almeno le dimensioni di una struttura [**\_ \_ AFFINITY PROCESSORE SOCKET.**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity)

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Puntatore a una variabile che riceve le dimensioni, in byte, dei dati archiviati nel buffer di output.

Se il buffer di output è troppo piccolo, la chiamata ha esito negativo, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [**WSAEINVAL**](windows-sockets-error-codes-2.md)e il parametro *lpcbBytesReturned* punta a un valore *DWORD* pari a zero.

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

Puntatore a una [**struttura WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) che deve essere utilizzata dal provider in una chiamata successiva a [**WPUQueueApc.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)
Il provider deve archiviare la struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a cui si fa riferimento (non il puntatore allo stesso) fino a quando non viene restituita [**la funzione WPUQueueApc.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)

**Nota:**  Questo parametro si applica solo alla **funzione WSPIoctl.**

### <a name="lperrno"></a>lpErrno

Puntatore al codice di errore.

**Nota:**  Questo parametro si applica solo alla **funzione WSPIoctl.**

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, la [**funzione WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce zero.

Se l'operazione ha esito negativo o è in sospeso, la [**funzione WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce **SOCKET \_ ERROR**.
Per ottenere informazioni estese sugli errori, chiamare [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).

| Codice di errore | Significato |
|------------|---------|
| **ERRORE \_ BUFFER \_ INSUFFICIENTE** | L'area dati passata a una chiamata di sistema è troppo piccola. Questo errore viene restituito se il buffer a cui punta il *parametro lpvOutBuffer* con una dimensione del buffer passata nel *parametro cbOutBuffer* è troppo piccolo. Le dimensioni del buffer necessarie verranno restituite nel *parametro lpcbBytesReturned.* Questo errore viene restituito se il *parametro cbOutBuffer* è minore delle dimensioni di una struttura [**\_ \_ AFFINITY DEL PROCESSORE SOCKET.**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) |
| **I/O WSA \_ \_ IN SOSPESO** | Un'operazione sovrapposta è stata avviata correttamente e il completamento verrà indicato in un secondo momento. |
| **OPERAZIONE WSA \_ \_ INTERROTTA** | Un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del **comando SIO \_ FLUSH** IOCTL. |
| **WSAEFAULT** | Il parametro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *lpCompletionRoutine* non è completamente contenuto in una parte valida dello spazio indirizzi utente. |
| **WSAEINPROGRESS** | La funzione viene richiamata quando è in corso un callback. |
| **WSAEINTR** | Un'operazione di blocco è stata interrotta. |
| **WSAEINVAL** | Il *parametro dwIoControlCode* non è un comando valido oppure un parametro di input specificato non è accettabile oppure il comando non è applicabile al tipo di socket specificato. Questo errore viene restituito se il *parametro cbOutBuffer* è minore delle dimensioni di una struttura [**\_ \_ AFFINITY DEL PROCESSORE SOCKET.**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity)
| **WSAENETDOWN** | Il sottosistema di rete non è riuscito. |
| **WSAENOPROTOOPT** | L'opzione socket non è supportata nel protocollo specificato. |
| **WSAENOTCONN** | Il socket *s* non è connesso. |
| **Wsaenotsock** | Il descrittore *s* non è un socket. |
| **WSAEOPNOTSUPP** | Il comando IOCTL specificato non è supportato. Questo errore viene restituito se **SIO \_ QUERY RSS PROCESSOR \_ \_ \_ INFO** IOCTL non è supportato dal provider di trasporto. |

## <a name="remarks"></a>Commenti

**SIO \_ QUERY \_ RSS PROCESSOR \_ \_ INFO** IOCTL è supportato in Windows 8 e Windows Server 2012 e versioni successive del sistema operativo.

**SIO \_ QUERY RSS PROCESSOR \_ \_ \_ INFO** IOCTL viene usato per determinare l'associazione tra un socket e un core del processore RSS e un nodo NUMA.
Questo IOCTL restituisce una struttura [**\_ \_ AFFINITY DEL PROCESSORE SOCKET**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) che contiene il [**NUMERO PROCESSORE \_**](/windows/desktop/api/winnt/ns-winnt-processor_number) e l'ID nodo NUMA.
La struttura [**PROCESSOR \_ NUMBER**](/windows/desktop/api/winnt/ns-winnt-processor_number) restituita contiene un numero di gruppo e un numero di processore relativo all'interno del gruppo.

Se il socket è un socket UDP, il socket deve essere connesso per il corretto funzionamento di **SIO \_ QUERY RSS PROCESSOR \_ \_ \_ INFO** IOCTL.

## <a name="see-also"></a>Vedi anche

[**PROCESSOR_NUMBER**](/windows/desktop/api/winnt/ns-winnt-processor_number)

[**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**SOCKET_PROCESSOR_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**Wsaioctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
