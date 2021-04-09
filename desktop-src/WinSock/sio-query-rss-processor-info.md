---
description: Il codice di controllo esegue una query sull'associazione tra un socket e un core del processore RSS e un nodo NUMA.
ms.assetid: DAF18C92-B479-474F-B438-0746CBA20653
title: Codice di controllo SIO_QUERY_RSS_PROCESSOR_INFO
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: a2d251fa4fee996adaec51599e7b1d140a296b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966673"
---
# <a name="sio_query_rss_processor_info-control-code"></a>Codice di controllo SIO_QUERY_RSS_PROCESSOR_INFO

## <a name="description"></a>Descrizione

Il codice di controllo delle **\_ \_ \_ \_ informazioni del processore RSS della query sio** esegue una query sull'associazione tra un socket e un core del processore RSS e un nodo NUMA.

Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.

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
Usare **le \_ \_ informazioni sul \_ processore \_ RSS della query sio** per questa operazione.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntatore al buffer di input.
Questo parametro non è utilizzato per questa operazione.

### <a name="cbinbuffer"></a>cbInBuffer

Dimensione, in byte, del buffer di input.
Questo parametro non è utilizzato per questa operazione.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntatore al buffer di output.
Questo parametro deve puntare a una struttura di [**\_ \_ affinità del processore di socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) se i parametri *lpOverlapped* e *il lpCompletionRoutine* sono **null**.

### <a name="cboutbuffer"></a>cbOutBuffer

Dimensione, in byte, del buffer di output.
Questo parametro deve essere almeno pari alla dimensione di una struttura di [**\_ \_ affinità del processore di socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) .

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Puntatore a una variabile che riceve le dimensioni, in byte, dei dati archiviati nel buffer di output.

Se il buffer di output è troppo piccolo, la chiamata ha esito negativo, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [**WSAEINVAL**](windows-sockets-error-codes-2.md)e il parametro *LpcbBytesReturned* punta a un valore *DWORD* pari a zero.

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

Puntatore a una struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) che deve essere usata dal provider in una chiamata successiva a [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).
Il provider deve archiviare la struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a cui si fa riferimento (non il puntatore alla stessa) finché non viene restituito il risultato della funzione [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) .

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
| **ERRORE \_ buffer insufficiente \_** | L'area dati passata a una chiamata di sistema è troppo piccola. Questo errore viene restituito se il buffer a cui punta il parametro *lpvOutBuffer* con una dimensione del buffer passata nel parametro *cbOutBuffer* è troppo piccolo. La dimensione del buffer richiesta verrà restituita nel parametro *lpcbBytesReturned* . Questo errore viene restituito se il parametro *cbOutBuffer* è minore della dimensione di una struttura [**di \_ \_ affinità del processore di socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) . |
| **\_io WSA \_ in sospeso** | Un'operazione sovrapposta è stata avviata correttamente e il completamento verrà indicato in un secondo momento. |
| **\_operazione WSA \_ interrotta** | Un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del comando IOCTL **\_ Flush sio** . |
| **WSAEFAULT** | Il parametro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *il lpCompletionRoutine* non è interamente contenuto in una parte valida dello spazio degli indirizzi utente. |
| **WSAEINPROGRESS** | La funzione viene richiamata quando è in corso un callback. |
| **WSAEINTR** | Un'operazione di blocco è stata interrotta. |
| **WSAEINVAL** | Il parametro *dwIoControlCode* non è un comando valido oppure un parametro di input specificato non è accettabile oppure il comando non è applicabile al tipo di socket specificato. Questo errore viene restituito se il parametro *cbOutBuffer* è minore della dimensione di una struttura [**di \_ \_ affinità del processore di socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) .
| **WSAENETDOWN** | Il sottosistema di rete non è riuscito. |
| **WSAENOPROTOOPT** | L'opzione socket non è supportata nel protocollo specificato. |
| **WSAENOTCONN** | Il socket *s* non è connesso. |
| **WSAENOTSOCK** | Il descrittore *s* non è un socket. |
| **ILWSAEOPNOTSUPP** | Il comando IOCTL specificato non è supportato. Questo errore viene restituito se le **\_ informazioni sul \_ \_ processore RSS \_ della query sio** non sono supportate dal provider di trasporto. |

## <a name="remarks"></a>Commenti

Le **\_ informazioni sul \_ \_ processore RSS \_ della query sio** sono supportate in Windows 8 e Windows Server 2012 e versioni successive del sistema operativo.

Le **\_ informazioni sul \_ \_ processore RSS \_ della query sio** vengono usate per determinare l'associazione tra un socket e un core del processore RSS e un nodo NUMA.
Questo IOCTL restituisce una struttura di [**\_ \_ affinità del processore di socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) che contiene il [**\_ numero del processore**](/windows/desktop/api/winnt/ns-winnt-processor_number) e l'ID del nodo NUMA.
La struttura [**del \_ numero di processore**](/windows/desktop/api/winnt/ns-winnt-processor_number) restituito contiene un numero di gruppo e un numero di processore relativo all'interno del gruppo.

Se il socket è un socket UDP, è necessario che il socket sia connesso per il corretto funzionamento del comando IOCTL per le **\_ \_ \_ \_ informazioni sul processore RSS della query sio** .

## <a name="see-also"></a>Vedi anche

[**PROCESSOR_NUMBER**](/windows/desktop/api/winnt/ns-winnt-processor_number)

[**presa**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**SOCKET_PROCESSOR_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
