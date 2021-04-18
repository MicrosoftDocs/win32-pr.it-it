---
description: Il codice di controllo Recupera il valore del backlog di invio ideale per la connessione sottostante.
ms.assetid: 03fe964b-26f7-4af7-83bf-62cc877d01a8
title: Codice di controllo SIO_IDEAL_SEND_BACKLOG_QUERY
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 440e42477a8939a62eeb84b800c0fd8feead5aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315781"
---
# <a name="sio_ideal_send_backlog_query-control-code"></a>Codice di controllo SIO_IDEAL_SEND_BACKLOG_QUERY

## <a name="description"></a>Descrizione

Il codice di controllo della **\_ query del \_ \_ backlog \_ di invio ideale per sio** Recupera il valore di backlog di invio ideale per la connessione sottostante.

Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_QUERY, // dwIoControlCode
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
  SIO_IDEAL_SEND_BACKLOG_QUERY, // dwIoControlCode
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
Usare **la \_ \_ query del \_ backlog \_ di invio ideale di sio** per questa operazione.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntatore al buffer di input.
Questo parametro non è utilizzato per questa operazione.

### <a name="cbinbuffer"></a>cbInBuffer

Dimensione, in byte, del buffer di input.
Questo parametro non è utilizzato per questa operazione.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntatore al buffer di output.
Questo parametro deve puntare a un tipo di dati **ULONG** se i parametri *lpOverlapped* e *il lpCompletionRoutine* sono **null**.

### <a name="cboutbuffer"></a>cbOutBuffer

Dimensione, in byte, del buffer di output.
Questo parametro deve essere almeno la dimensione di un tipo di dati **ULONG** .

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
| **WSAEFAULT** | Il parametro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *il lpCompletionRoutine* non è interamente contenuto in una parte valida dello spazio degli indirizzi utente. |
| **WSAEINPROGRESS** | La funzione viene richiamata quando è in corso un callback. |
| **WSAEINTR** | Un'operazione di blocco è stata interrotta. |
| **WSAEINVAL** | Il parametro *dwIoControlCode* non è un comando valido oppure un parametro di input specificato non è accettabile oppure il comando non è applicabile al tipo di socket specificato. Questo errore viene restituito se il parametro *cbOutBuffer* è minore della dimensione di un tipo di dati **ULONG** .
| **WSAENETDOWN** | Il sottosistema di rete non è riuscito. |
| **WSAENOPROTOOPT** | L'opzione socket non è supportata nel protocollo specificato. |
| **WSAENOTCONN** | Il Socket s non è connesso. |
| **WSAENOTSOCK** | Il descrittore *s* non è un socket. |
| **ILWSAEOPNOTSUPP** | Il comando IOCTL specificato non è supportato. Questo errore viene restituito se la **\_ query di \_ \_ backlog di \_ invio ideale di sio** non è supportata dal provider di trasporto. Questo errore viene restituito anche quando viene eseguito un tentativo di usare la **\_ query di \_ \_ backlog \_ di invio ideale di sio** per un socket di datagramma. |

## <a name="remarks"></a>Commenti

La **\_ query del \_ \_ backlog di \_ invio ideale di sio** è supportata in Windows Server 2008, Windows Vista con Service Pack 1 (SP1) e versioni successive del sistema operativo.

Quando si inviano dati tramite una connessione TCP mediante Windows Sockets, è importante garantire una quantità sufficiente di dati in attesa (inviati ma non ancora riconosciuti) in TCP per ottenere la massima velocità effettiva.
Il valore ideale per la quantità di dati in attesa di ottenere la migliore velocità effettiva per la connessione TCP è denominato dimensione del backlog di invio ideale.
Il valore ISB è una funzione del prodotto di ritardo della larghezza di banda della connessione TCP e della finestra di ricezione annunciata del ricevitore (e parzialmente la quantità di congestione nella rete).

Il valore ISB per connessione è disponibile nell'implementazione del protocollo TCP in Windows Server 2008, Windows Vista con SP1 e versioni successive del sistema operativo.
La **\_ query del \_ \_ backlog di \_ invio ideale di sio** può essere usata da un'applicazione per ricevere una notifica quando il valore di ISB cambia in modo dinamico per una connessione.

In Windows Server 2008, Windows Vista con SP1 e versioni successive del sistema operativo, la modifica del [**\_ backlog di \_ INVIO \_ del \_ backlog ideale di sio**](sio-ideal-send-backlog-change.md) e la **query del \_ \_ backlog di invio \_ \_ ideale di sio** sono supportate nei socket orientati al flusso che si trovano in uno stato connesso.

L'intervallo per il valore ISB per una connessione TCP può teoricamente variare da 0 a un massimo di 16 megabyte.

L'utilizzo tipico della [**modifica del \_ \_ backlog di \_ INVIO \_ ideale di sio**](sio-ideal-send-backlog-change.md) e della **\_ \_ \_ \_ query di backlog di invio ideale di sio** è basato sul metodo Send usato dalle applicazioni.
Vengono illustrati due casi comuni.

Le applicazioni che eseguono una richiesta di invio bloccante o non bloccante alla volta in genere si basano sul buffer di invio interno da Winsock per ottenere una velocità effettiva decente.
Il limite del buffer di invio per una determinata connessione è controllato dall'opzione socket **\_ sndbuf** .
Per il metodo Send bloccante e non bloccante, il limite del buffer di invio determina la quantità di dati mantenuti in attesa in TCP.
Se il valore ISB per la connessione è superiore al limite del buffer di invio, la velocità effettiva consentita per la connessione non è ottimale.
Per ottenere una velocità effettiva migliore, le applicazioni possono impostare il limite del buffer di invio in base al risultato della query ISB, in quanto si verificano notifiche di modifica ISB sulla connessione.

Per le applicazioni che utilizzano il metodo di invio sovrapposto con più richieste di invio in attesa, la quantità di dati mantenuti in attesa in TCP è determinata dal limite del buffer di invio in Winsock e dalla quantità totale di dati contenuti nelle richieste di invio sovrapposte in attesa.
In questo caso, le applicazioni devono usare il valore ISB per determinare il numero di richieste di invio in attesa da tenere e le dimensioni dei dati per ogni richiesta di invio.
Idealmente, l'applicazione deve provare a tenere soddisfatta l'equazione seguente:

`ISB value == send buffer limit + (number of simultaneous overlapped send requests * data length per send request)`

Si noti che l'utilizzo delle IOCTL ISB sui socket TCP nel modo precedente può comportare un aumento dell'utilizzo della memoria in Exchange per una maggiore velocità effettiva nelle connessioni con un prodotto con ritardo della larghezza di banda elevato.
L'implementazione TCP in Windows limiterà i valori ISB secondo le necessità in base all'utilizzo complessivo della memoria di sistema.

La **\_ query di \_ \_ backlog di \_ invio ideale di sio** è consentita solo su un socket del flusso che si trova nello stato connesso.
In caso contrario, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** avrà esito negativo con **WSAENOTCONN**.

Qualsiasi IOCTL può bloccarsi per un periodo illimitato, a seconda dell'implementazione del provider di servizi.
Se l'applicazione non è in grado di tollerare il blocco in una chiamata di funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** , si consiglia di eseguire l'i/O sovrapposto per le IOCTL che sono particolarmente probabilmente bloccate.

La **\_ query del \_ \_ backlog di \_ invio ideale per sio** non può essere bloccata in modo da essere normalmente chiamata in modo sincrono con i parametri *lpOverlapped* e *il lpCompletionRoutine* impostati su **null**.

La **\_ query del \_ \_ backlog di \_ invio ideale di sio** può avere esito negativo con l'operazione **WSAEINTR** o **WSA \_ \_ interrotta** nei casi seguenti:

La connessione TCP viene normalmente disconnessa nella direzione di invio.
Questo problema può verificarsi in seguito a una chiamata alla funzione Shutdown con il parametro how impostato su **SD \_ Send**, una chiamata alla funzione **DisconnectEx** o una chiamata alla funzione **TransmitFile** o **TransmitPackets** con il parametro *dwFlags* impostato su **tf \_ Disconnect** o **tf \_ riuso**.
La connessione TCP è stata reimpostata o interrotta.
La richiesta viene annullata dal gestore di I/O.

Due funzioni wrapper inline per tali IOCTL sono definite nel file di intestazione *Ws2tcpip. h* .
Si consiglia di usare queste funzioni inline invece di usare la modifica del [**\_ backlog di \_ INVIO \_ \_**](sio-ideal-send-backlog-change.md) e la **\_ \_ \_ \_ query** di backlog di invio ideale per Sio, direttamente.

La funzione wrapper inline per la [**\_ modifica del \_ \_ backlog di \_ invio ideale di sio**](sio-ideal-send-backlog-change.md) è la funzione **idealsendbacklognotify** .

La funzione wrapper inline per la **\_ query di \_ \_ backlog di \_ invio ideale di sio** è la funzione **idealsendbacklogquery** .

Il buffer di invio dinamico per TCP è stato aggiunto in Windows 7 e Windows Server 2008 R2.
Per impostazione predefinita, il buffer di invio dinamico per TCP è abilitato, a meno che un'applicazione non imposti l'opzione **\_ sndbuf** socket sul socket di flusso.

L'utilizzo di netsh è il metodo consigliato per eseguire query o impostare il buffer di invio dinamico per TCP.

Il valore corrente per il buffer di invio dinamico per TCP può essere recuperato con il comando seguente:

`netsh winsock show autotuning`

Il buffer di invio dinamico per TCP può essere disabilitato usando il comando seguente:

`netsh winsock set autotuning off`

Il buffer di invio dinamico per TCP può essere abilitato usando il comando seguente:

`netsh winsock set autotuning on`

Sebbene sia sconsigliato, il buffer di invio dinamico può essere disabilitato da un'applicazione impostando il valore del registro di sistema seguente su zero:

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\AFD\Parameters\DynamicSendBufferDisable`

Quando si modifica il valore del buffer di invio dinamico utilizzando NetSh.exe o modificando il valore del registro di sistema, è necessario riavviare il computer per rendere effettive le modifiche.

Con il buffering di invio dinamico in Windows 7 e Windows Server 2008 R2, l'uso [**della \_ modifica del backlog di invio del \_ \_ \_ backlog ideale**](sio-ideal-send-backlog-change.md) di SIO e della **query del \_ \_ \_ backlog \_ di invio ideale di sio** è necessario solo in circostanze particolari.

## <a name="see-also"></a>Vedi anche

[**SIO_IDEAL_SEND_BACKLOG_CHANGE**](sio-ideal-send-backlog-change.md)

[**presa**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
