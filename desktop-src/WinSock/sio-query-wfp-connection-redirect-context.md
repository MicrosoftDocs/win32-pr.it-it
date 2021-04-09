---
description: Il codice di controllo Recupera il contesto di reindirizzamento per un record di reindirizzamento utilizzato da un servizio di reindirizzamento della piattaforma filtro Windows.
ms.assetid: 87DB11BB-E08D-49DF-A211-133D813373E0
title: Codice di controllo SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 1e5e5f6c56411ada1e87e8cdf240a89f9c293e4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129127"
---
# <a name="sio_query_wfp_connection_redirect_context-control-code"></a>Codice di controllo SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT

## <a name="description"></a>Descrizione

Il codice di controllo del **\_ contesto di \_ \_ \_ Reindirizzamento \_ della connessione per la query sio** Recupera il contesto di reindirizzamento per un record di reindirizzamento usato da un servizio di reindirizzamento della piattaforma filtro Windows (WFP).

Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.

```cpp
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT, // dwIoControlCode
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
  SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT, // dwIoControlCode
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
Usare **il \_ \_ contesto di \_ \_ Reindirizzamento della \_ connessione WFP per la query sio** per questa operazione.

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
| **\_io WSA \_ in sospeso** | Un'operazione sovrapposta è stata avviata correttamente e il completamento verrà indicato in un secondo momento. |
| **\_operazione WSA \_ interrotta** | Un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del comando IOCTL SIO_FLUSH. |
| **WSAEFAULT** | Il parametro *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *il lpCompletionRoutine* non è interamente contenuto in una parte valida dello spazio degli indirizzi utente. |
| **WSAEINPROGRESS** | La funzione viene richiamata quando è in corso un callback. |
| **WSAEINTR** | Un'operazione di blocco è stata interrotta. |
| **WSAEINVAL** | Il parametro *dwIoControlCode* non è un comando valido oppure un parametro di input specificato non è accettabile oppure il comando non è applicabile al tipo di socket specificato. Questo errore viene restituito se il parametro *cbOutBuffer* è minore della dimensione di un tipo di dati **ULONG** . |
| **WSAENETDOWN** | Il sottosistema di rete non è riuscito. |
| **WSAENOPROTOOPT** | L'opzione socket non è supportata nel protocollo specificato. |
| **WSAENOTCONN** | Il socket *s* non è connesso. |
| **WSAENOTSOCK** | Il descrittore *s* non è un socket. |
| **ILWSAEOPNOTSUPP** | Il comando IOCTL specificato non è supportato. Questo errore viene restituito se il **\_ contesto di \_ \_ \_ Reindirizzamento \_ della connessione** per la query di sio non è supportato dal provider di trasporto. |

## <a name="remarks"></a>Commenti

Il **contesto IOCTL di \_ \_ \_ \_ Reindirizzamento della \_ connessione di query sio** è supportato in Windows 8 e Windows Server 2012 e versioni successive del sistema operativo.

Il WFP consente di accedere al percorso di elaborazione dei pacchetti TCP/IP, in cui è possibile esaminare o modificare i pacchetti in uscita e in ingresso prima di consentire l'ulteriore elaborazione.
Toccando il percorso di elaborazione TCP/IP, i fornitori di software indipendenti (ISV) possono creare più facilmente firewall, software antivirus, software di diagnostica e altri tipi di applicazioni e servizi.
PAM fornisce componenti in modalità utente e kernel, in modo che gli ISV di terze parti possano partecipare alle decisioni di filtro che avvengono a diversi livelli nello stack di protocolli TCP/IP e in tutto il sistema operativo.
La funzionalità di reindirizzamento della connessione WFP consente a un driver del kernel di callout di WFP di reindirizzare una connessione localmente a un processo in modalità utente, di eseguire l'ispezione dei contenuti in modalità utente e inoltrare il contenuto ispezionato utilizzando una connessione diversa alla destinazione originale.

La **\_ query sio \_ \_ contesto di \_ Reindirizzamento \_ della connessione WFP** e molti altri IOCTL correlati sono componenti in modalità utente utilizzati per consentire a più applicazioni proxy di connessione basate su WFP di ispezionare lo stesso flusso di traffico in modo cooperativo.
Ogni agente di ispezione può verificare in modo sicuro il traffico di rete che è già stato ispezionato da un altro agente di ispezione.
Con la presenza di più proxy (sviluppati da ISV diversi, ad esempio) la connessione utilizzata da un proxy per comunicare con la destinazione finale può a sua volta essere reindirizzata da un secondo proxy e la nuova connessione potrebbe essere reindirizzata dal proxy originale.
Senza il rilevamento della connessione, la connessione originale potrebbe non raggiungere mai la destinazione finale poiché rimane bloccata in un ciclo del proxy infinito.

L'IOCTL del **\_ contesto di \_ \_ \_ Reindirizzamento \_ della connessione della query sio** viene usato per consentire a più applicazioni proxy di connessione basate su WFP di ispezionare lo stesso flusso di traffico in modo cooperativo.
Ogni agente di ispezione può verificare in modo sicuro il traffico di rete che è già stato ispezionato da un altro agente di ispezione.
Con la presenza di più proxy (sviluppati da ISV diversi, ad esempio) la connessione utilizzata da un proxy per comunicare con la destinazione finale può a sua volta essere reindirizzata da un secondo proxy e la nuova connessione potrebbe essere reindirizzata dal proxy originale.
Senza il rilevamento della connessione, la connessione originale potrebbe non raggiungere mai la destinazione finale poiché rimane bloccata in un ciclo del proxy infinito.
L'IOCTL del **\_ contesto di \_ \_ \_ Reindirizzamento \_ della connessione per la query sio** viene usato per fornire il rilevamento delle connessioni con proxy sulle connessioni socket reindirizzate.
Questa funzionalità WFP facilita il rilevamento dei record di reindirizzamento dal reindirizzamento iniziale di una connessione alla connessione finale alla destinazione.

I **\_ record di \_ \_ \_ Reindirizzamento \_ della connessione per la query sio** vengono usati da un servizio di reindirizzamento basato su WFP per recuperare il record di reindirizzamento dalla connessione del pacchetto TCP/IP accettata (ad esempio, il socket connesso per un socket TCP o un socket UDP) reindirizzato al relativo callout in modalità kernel registrato in **ale Connect livelli di \_ \_ Reindirizzamento** in un driver in modalità kernel.
Il **\_ \_ \_ \_ \_ contesto** di reindirizzamento della connessione per la query sio viene usato da un servizio di reindirizzamento basato su WFP per recuperare il contesto di reindirizzamento per un record di reindirizzamento dalla connessione del pacchetto TCP/IP accettata (ad esempio, il socket connesso per un socket TCP o un socket UDP) reindirizzato a esso dal callout complementare registrato a **ALE_CONNECT_REDIRECT** livelli.
Il contesto di reindirizzamento è facoltativo e viene usato se lo stato del reindirizzamento corrente di una connessione è che la connessione è stata reindirizzata dal servizio di reindirizzamento chiamante oppure la connessione è stata reindirizzata in precedenza dal servizio di reindirizzamento chiamante, ma in seguito reindirizzato da un servizio di reindirizzamento diverso.
Il servizio di reindirizzamento trasferisce il record di reindirizzamento recuperato al socket TCP usato per eseguire il proxy del contenuto originale usando il **set di dati di \_ Reindirizzamento della connessione sio set \_ WFP \_ \_ \_** .

Poiché il contesto di reindirizzamento di WFP è un BLOB di dati a lunghezza variabile impostato dal servizio di reindirizzamento, il chiamante può fornire un buffer di output di grandi dimensioni (ad esempio, un buffer 1K a cui punta il parametro *lpvOutBuffer* ) oppure può passare come dimensione del buffer di output nel parametro *cbOutBuffer* di 0 per eseguire una query sulle dimensioni del buffer necessarie per memorizzare il BLOB restituito.
Se la dimensione del buffer di output non è sufficiente per contenere i dati, le funzioni [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituiranno un **errore di \_ \_ buffer insufficiente** e le dimensioni del buffer richieste verranno restituite nel valore a cui punta il parametro *lpcbBytesReturned* .

L'applicazione che chiama **la \_ query sio \_ WF \ P_CONNECTION \_ reindirizza i \_ record** IOCTL non deve comprendere il BLOB contenente i record di reindirizzamento recuperati.
Si tratta di un BLOB opaco di dati che l'applicazione deve recuperare e passare nuovamente al nuovo socket.

## <a name="see-also"></a>Vedi anche

[**Opzioni di IPPROTO_IP socket**](/windows/desktop/winsock/ipproto-ip-socket-options)

[**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md)

[**SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS**](sio-set-wfp-connection-redirect-records.md)

[**presa**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
