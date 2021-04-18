---
description: Il codice di controllo imposta il record di reindirizzamento sul nuovo socket TCP usato per la connessione del servizio di reindirizzamento.
ms.assetid: 0AC78ED4-A6EC-4D62-919C-1EF7CDE8EE80
title: Codice di controllo SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 11ce07c94104ecd986dc117b00dba2a49a7b5dc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315778"
---
# <a name="sio_set_wfp_connection_redirect_records-control-code"></a>Codice di controllo SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS

## <a name="description"></a>Descrizione

Il codice di controllo dei **record di reindirizzamento della connessione di sio \_ set \_ WFP \_ \_ \_** imposta il record di reindirizzamento sul nuovo socket TCP usato per la connessione alla destinazione finale per l'uso da parte di un servizio di reindirizzamento della piattaforma filtro Windows (WFP).

Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.

```cpp
int WSAIoctl(
  (socket) s,                              // descriptor identifying a socket
  SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  (LPVOID) lpvInputBuffer,                 // lpvInBuffer
  (DWORD) cbInputBuffer,                   // cbInBuffer
  NULL,                                    // output buffer
  0,                                       // size of output buffer
  (LPDWORD) lpcbBytesReturned,             // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,          // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine, // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,                              // descriptor identifying a socket
  SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  (LPVOID) lpvInputBuffer,                 // lpvInBuffer
  (DWORD) cbInputBuffer,                   // cbInBuffer
  NULL,                                    // output buffer
  0,                                       // size of output buffer
  (LPDWORD) lpcbBytesReturned,             // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,          // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,              // a WSATHREADID structure
  (LPINT) lpErrno                          // a pointer to the error code.
);
```

## <a name="parameters"></a>Parametri

### <a name="s"></a>s

Descrittore che identifica un socket.

### <a name="dwiocontrolcode"></a>dwIoControlCode

Codice di controllo per l'operazione.
Usare i **record di reindirizzamento della connessione di sio \_ set \_ WFP \_ \_ \_** per questa operazione.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntatore al buffer di input.
Questo parametro contiene un puntatore al record di reindirizzamento di WFP associato al socket.

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
| **\_io WSA \_ in sospeso** | Operazione di I/O sovrapposta in corso. Questo valore viene restituito se un'operazione sovrapposta è stata avviata correttamente e il completamento verrà indicato in un secondo momento. |
| **\_operazione WSA \_ interrotta** | L'operazione di I/O è stata interrotta a causa dell'uscita di un thread o di una richiesta dell'applicazione. Questo errore viene restituito se un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del comando IOCTL **SIO_FLUSH** . |
| **WSAEACCES** | È stato effettuato un tentativo di accesso a un socket in modo non consentito dalle autorizzazioni di accesso. Questo errore viene restituito in diverse condizioni che includono quanto segue: l'utente non dispone dei privilegi amministrativi necessari sul computer locale o l'applicazione non è in esecuzione in una shell avanzata come amministratore predefinito ( `RunAs administrator` ). |
| **WSAEFAULT** | Il sistema ha rilevato un indirizzo puntatore non valido durante il tentativo di usare un argomento puntatore in una chiamata. Questo errore viene restituito dal parametro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *il lpCompletionRoutine* non è interamente contenuto in una parte valida dello spazio degli indirizzi utente. |
| **WSAEINPROGRESS** | È in corso un'operazione di blocco. Questo errore viene restituito se la funzione viene richiamata quando è in corso un callback. |
| **WSAEINTR** | Un'operazione di blocco è stata interrotta da una chiamata a **WSACancelBlockingCall**. Questo errore viene restituito se un'operazione di blocco è stata interrotta. |
| **WSAEINVAL** | Argomento fornito non valido. Questo errore viene restituito se il parametro *dwIoControlCode* non è un comando valido o se un parametro di input specificato non è accettabile o se il comando non è applicabile al tipo di socket specificato. |
| **WSAENETDOWN** | Rete inattiva rilevata durante l'operazione del socket. Questo errore viene restituito se il sottosistema di rete non è riuscito. |
| **WSAENOTSOCK** | Si è tentato di eseguire un'operazione su un elemento che non è un socket. Questo errore viene restituito se il descrittore *s* non è un socket. |
| **ILWSAEOPNOTSUPP** | L'operazione tentata non è supportata per il tipo di oggetto a cui si fa riferimento. Questo errore viene restituito se il comando IOCTL specificato non è supportato. Questo errore viene restituito anche se il **\_ set di \_ dati di \_ \_ Reindirizzamento \_ della connessione di sio set WFP** non è supportato dal provider di trasporto. |

## <a name="remarks"></a>Commenti

Il **\_ set di \_ dati di \_ \_ Reindirizzamento \_ della connessione di sio set WFP** è supportato in Windows 8 e Windows Server 2012 e versioni successive del sistema operativo.

Il WFP consente di accedere al percorso di elaborazione dei pacchetti TCP/IP, in cui è possibile esaminare o modificare i pacchetti in uscita e in ingresso prima di consentire l'ulteriore elaborazione.
Toccando il percorso di elaborazione TCP/IP, i fornitori di software indipendenti (ISV) possono creare più facilmente firewall, software antivirus, software di diagnostica e altri tipi di applicazioni e servizi.
PAM fornisce componenti in modalità utente e kernel, in modo che gli ISV di terze parti possano partecipare alle decisioni di filtro che avvengono a diversi livelli nello stack di protocolli TCP/IP e in tutto il sistema operativo.
La funzionalità di reindirizzamento della connessione WFP consente a un driver del kernel di callout di WFP di reindirizzare una connessione localmente a un processo in modalità utente, di eseguire l'ispezione dei contenuti in modalità utente e inoltrare il contenuto ispezionato utilizzando una connessione diversa alla destinazione originale.

I **\_ record di reindirizzamento della connessione del set di \_ \_ \_ \_ dati di sio** e di molti altri IOCTL correlati sono componenti in modalità utente utilizzati per consentire a più applicazioni proxy di connessione basate su WFP di ispezionare lo stesso flusso di traffico in modo cooperativo.
Ogni agente di ispezione può verificare in modo sicuro il traffico di rete che è già stato ispezionato da un altro agente di ispezione.
Con la presenza di più proxy (sviluppati da ISV diversi, ad esempio) la connessione utilizzata da un proxy per comunicare con la destinazione finale può a sua volta essere reindirizzata da un secondo proxy e la nuova connessione potrebbe essere reindirizzata dal proxy originale.
Senza il rilevamento della connessione, la connessione originale potrebbe non raggiungere mai la destinazione finale poiché rimane bloccata in un ciclo del proxy infinito.

Il **\_ set di \_ dati di \_ \_ Reindirizzamento \_ della connessione di sio set WFP** viene usato per fornire il rilevamento delle connessioni con proxy sulle connessioni socket reindirizzate.
Questa funzionalità WFP facilita il rilevamento dei record di reindirizzamento dal reindirizzamento iniziale di una connessione alla connessione finale alla destinazione.

Il [**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md) IOCTL viene usato da un servizio di reindirizzamento basato su WFP per recuperare il record di reindirizzamento dalla connessione del pacchetto TCP/IP accettata, ad esempio il socket connesso per un socket TCP o un socket UDP, ad esempio, reindirizzato al relativo callout in modalità kernel registrato nei livelli di  **\_ \_ Reindirizzamento di ale Connect** in un driver in modalità kernel.
Il [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) IOCTL recupera il contesto di reindirizzamento per un record di reindirizzamento, che viene usato.
Il contesto di reindirizzamento è facoltativo e viene usato se lo stato del reindirizzamento corrente di una connessione è che la connessione è stata reindirizzata dal servizio di reindirizzamento chiamante oppure la connessione è stata reindirizzata in precedenza dal servizio di reindirizzamento chiamante, ma in seguito reindirizzato da un servizio di reindirizzamento diverso. Il servizio di reindirizzamento trasferisce il record di reindirizzamento recuperato al socket TCP usato per eseguire il proxy del contenuto originale usando il **set di dati di \_ Reindirizzamento della connessione sio set \_ WFP \_ \_ \_** .

Non è necessario che l'applicazione che chiama il **set di dati di reindirizzamento della connessione del set di \_ \_ \_ \_ \_ dati** per il comando IOCTL contenga il BLOB contenente il record di Reindirizzamento da impostare.
Si tratta di un BLOB opaco di dati che l'applicazione deve passare nuovamente al nuovo socket.

## <a name="see-also"></a>Vedi anche

[**Opzioni di IPPROTO_IP socket**](/windows/desktop/winsock/ipproto-ip-socket-options)

[**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md)

[**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md)

[**presa**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
