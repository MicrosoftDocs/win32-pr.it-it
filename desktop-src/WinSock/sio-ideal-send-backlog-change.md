---
description: Il codice di controllo notifica a un'applicazione quando viene modificato il valore di backlog di invio ideale per la connessione.
ms.assetid: 337883a5-7ceb-40d3-b318-b86dd488b94a
title: Codice di controllo SIO_IDEAL_SEND_BACKLOG_CHANGE
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 4eb07efecd39774c60d47cbcf7245c5831760e06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755071"
---
# <a name="sio_ideal_send_backlog_change-control-code"></a>Codice di controllo SIO_IDEAL_SEND_BACKLOG_CHANGE

## <a name="description"></a>Descrizione

Il codice di controllo delle **\_ modifiche del backlog di invio ideale per sio \_ Invia \_ \_** una notifica all'applicazione quando viene modificato il valore di backlog di invio ideale per la connessione.

Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_CHANGE, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_CHANGE, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  NULL,         // output buffer
  0,       // size of output buffer
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
Usare **la \_ \_ modifica del \_ backlog \_ di invio ideale di sio** per questa operazione.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntatore al buffer di input.
Questo parametro non è utilizzato per questa operazione.

### <a name="cbinbuffer"></a>cbInBuffer

Dimensione, in byte, del buffer di input. Questo parametro non è utilizzato per questa operazione.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntatore al buffer di output.
Questo parametro non è utilizzato per questa operazione.

### <a name="cboutbuffer"></a>cbOutBuffer

Dimensione, in byte, del buffer di output.
Questo parametro deve essere impostato su zero.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Puntatore a una variabile che riceve le dimensioni, in byte, dei dati archiviati nel buffer di output.
Il parametro restituito punta a un valore **DWORD** pari a zero per questa operazione, poiché non è presente alcun output.

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
| **\_io WSA \_ in sospeso** | Un'operazione sovrapposta è stata avviata correttamente e il completamento verrà indicato in un secondo momento. |
| **\_operazione WSA \_ interrotta** | Un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del comando IOCTL **\_ Flush sio** . |
| **WSAEFAULT** | Il parametro *lpOverlapped* o *il lpCompletionRoutine* non è interamente contenuto in una parte valida dello spazio degli indirizzi utente. |
| **WSAEINPROGRESS** | La funzione viene richiamata quando è in corso un callback. |
| **WSAEINTR** | Un'operazione di blocco è stata interrotta. |
| **WSAEINVAL** | Il parametro *dwIoControlCode* non è un comando valido oppure un parametro di input specificato non è accettabile oppure il comando non è applicabile al tipo di socket specificato. Questo errore viene restituito se il parametro *cbOutBuffer* è diverso da zero. |
| **WSAENETDOWN** | Il sottosistema di rete non è riuscito. |
| **WSAENOPROTOOPT** | L'opzione socket non è supportata nel protocollo specificato. |
| **WSAENOTCONN** | Il socket *s* non è connesso. |
| **WSAENOTSOCK** | Il descrittore *s* non è un socket. |
| **ILWSAEOPNOTSUPP** | Il comando IOCTL specificato non è supportato. Questo errore viene restituito se la **\_ modifica del \_ \_ backlog di \_ invio della soluzione sio ideale** non è supportata dal provider di trasporto. Questo errore viene restituito anche quando viene eseguito un tentativo di usare il comando di **modifica del backlog di invio della \_ soluzione sio ideale \_ \_ \_** su un socket di datagramma. |

## <a name="remarks"></a>Commenti

Il IOCTL ideale per la **\_ modifica del \_ \_ backlog \_ di invio** è supportato in Windows Server 2008, Windows Vista con Service Pack 1 (SP1) e versioni successive del sistema operativo.

Quando si inviano dati tramite una connessione TCP mediante Windows Sockets, è importante garantire una quantità sufficiente di dati in attesa (inviati ma non ancora riconosciuti) in TCP per ottenere la massima velocità effettiva.
Il valore ideale per la quantità di dati in attesa di ottenere la migliore velocità effettiva per la connessione TCP è denominato dimensione del backlog di invio ideale.
Il valore ISB è una funzione del prodotto di ritardo della larghezza di banda della connessione TCP e della finestra di ricezione annunciata del ricevitore (e parzialmente la quantità di congestione nella rete).

Il valore ISB per connessione è disponibile nell'implementazione del protocollo TCP in Windows Server 2008, Windows Vista con SP1 e versioni successive del sistema operativo.
La **\_ modifica del \_ \_ backlog di \_ invio ideale di sio** può essere usata da un'applicazione per ricevere una notifica quando il valore di ISB cambia in modo dinamico per una connessione.

In Windows Server 2008, Windows Vista con SP1 e versioni successive del sistema operativo, la modifica del **\_ backlog di \_ INVIO \_ del \_ backlog ideale di sio** e la [**query del \_ \_ backlog di invio \_ \_ ideale di sio**](sio-ideal-send-backlog-query.md) sono supportate nei socket orientati al flusso che si trovano in uno stato connesso.

L'intervallo per il valore ISB per una connessione TCP può teoricamente variare da 0 a un massimo di 16 megabyte.

Vedere la pagina di riferimento per la [**\_ query di \_ \_ backlog \_ di invio ideale per sio**](sio-ideal-send-backlog-query.md) per l'uso tipico del meccanismo ISB per ottenere una migliore velocità effettiva su connessioni di prodotti con ritardo della larghezza di banda elevata.

La **\_ modifica del \_ \_ backlog di \_ invio ideale di sio** è consentita solo su un socket di flusso che si trova nello stato connesso.
In caso contrario, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** avrà esito negativo con **WSAENOTCONN**.

La **\_ modifica del \_ \_ backlog di \_ invio della soluzione sio ideale** non utilizza buffer di input o di output e in sospeso né blocca fino a quando non viene apportata una modifica all'ISB nella connessione sottostante.
Quando questo comando IOCTL viene completato, un'applicazione Winsock può usare l'IOCTL [**\_ query di \_ \_ backlog \_ di invio ideale di sio**](sio-ideal-send-backlog-query.md) per recuperare il nuovo valore ISB sulla connessione.

La **\_ modifica del \_ \_ backlog di \_ invio della soluzione sio ideale** non supporta la modalità non di blocco.
Un'applicazione è autorizzata a eseguire questo IOCTL su un socket non bloccante, ma il IOCTL verrà semplicemente bloccato o sospeso fino a quando il valore di ISB non cambia.

Se entrambi i parametri *lpOverlapped* e *il lpCompletionRoutine* sono null, il socket in questa funzione verrà considerato come un socket non sovrapposto.
Per un socket non sovrapposto, i parametri *lpOverlapped* e *il lpCompletionRoutine* vengono ignorati, ad eccezione del fatto che la funzione può essere bloccata se socket *s* è in modalità di blocco.
Se il socket *s* è in modalità non di blocco, questa funzione verrà comunque bloccata poiché questo particolare IOCTL non supporta la modalità non di blocco.

Per i socket sovrapposti, le operazioni che non possono essere completate immediatamente verranno avviate e il completamento verrà indicato in un secondo momento.

Qualsiasi IOCTL può bloccarsi per un periodo illimitato, a seconda dell'implementazione del provider di servizi.
Se l'applicazione non è in grado di tollerare il blocco in una chiamata di funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** , si consiglia di eseguire l'i/O sovrapposto per le IOCTL che sono particolarmente probabilmente bloccate.

La **\_ modifica del \_ \_ backlog di \_ invio della soluzione sio ideale** fornisce una notifica e dovrebbe bloccarsi o essere sospesa fino a quando il valore di ISB non cambia.
Quindi, in genere verrebbe chiamato in modo asincrono con il parametro *lpOverlapped* impostato su una struttura WSAOVERLAPPED valida.

La **\_ modifica del \_ \_ backlog di \_ invio ideale di sio** può avere esito negativo con l'operazione **WSAEINTR** o **WSA \_ \_ interrotta** nei casi seguenti:

* La connessione TCP viene normalmente disconnessa nella direzione di invio. Questo problema può verificarsi in seguito a una chiamata alla funzione Shutdown con il parametro how impostato su **SD \_ Send**, una chiamata alla funzione **DisconnectEx** o una chiamata alla funzione **TransmitFile** o **TransmitPackets** con il parametro *dwFlags* impostato su **tf \_ Disconnect** o **tf \_ riuso**.
* La connessione TCP è stata reimpostata o interrotta.
* L'applicazione rilascia un comando IOCTL di **\_ invio della \_ \_ \_ modifica del backlog ideale** quando è già presente una richiesta di notifica in sospeso. È consentita solo la richiesta di **\_ modifica del \_ backlog di invio \_ \_ ideale** di 1 1 in sospeso alla volta.
* La richiesta viene annullata dal gestore di I/O.
* Il socket è chiuso.

Due funzioni wrapper inline per tali IOCTL sono definite nel file di intestazione *Ws2tcpip. h* .
Si consiglia di usare queste funzioni inline invece di usare la modifica del **\_ backlog di \_ INVIO \_ \_** e la [**\_ \_ \_ \_ query**](sio-ideal-send-backlog-query.md) di backlog di invio ideale per Sio, direttamente.

La funzione wrapper inline per la **\_ modifica del \_ \_ backlog di \_ invio ideale di sio** è la funzione **idealsendbacklognotify** .

La funzione wrapper inline per la [**\_ query di \_ \_ backlog di \_ invio ideale di sio**](sio-ideal-send-backlog-query.md) è la funzione **idealsendbacklogquery** .

## <a name="see-also"></a>Vedi anche

[**SIO_IDEAL_SEND_BACKLOG_QUERY**](sio-ideal-send-backlog-query.md)

[**presa**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
