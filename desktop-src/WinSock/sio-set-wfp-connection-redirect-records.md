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
ms.openlocfilehash: 5d8617f679907e46d8fc194bb75b9e5c2dac267a1c4781fc7cc0f1bf47d49d06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993361"
---
# <a name="sio_set_wfp_connection_redirect_records-control-code"></a>Codice di controllo SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS

## <a name="description"></a>Descrizione

Il codice di controllo **SIO \_ SET WFP CONNECTION REDIRECT \_ \_ \_ \_ RECORDS** imposta il record di reindirizzamento al nuovo socket TCP usato per la connessione alla destinazione finale per l'uso da parte di un servizio di reindirizzamento Windows Filtering Platform (WFP).

Per eseguire questa operazione, chiamare la [**funzione WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.

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
Usare **SIO \_ SET WFP CONNECTION REDIRECT RECORDS \_ \_ \_ \_ per** questa operazione.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntatore al buffer di input.
Questo parametro contiene un puntatore al record di reindirizzamento WFP associato al socket.

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

Se *lpOverlapped* è **NULL,** il **valore DWORD** a cui punta il *parametro lpcbBytesReturned* restituito in una chiamata riuscita non può essere zero.

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

Puntatore a una [**struttura WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) che deve essere utilizzata dal provider in una chiamata successiva a [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).
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
| **I/O WSA \_ \_ IN SOSPESO** | Operazione di I/O sovrapposta in corso. Questo valore viene restituito se un'operazione sovrapposta è stata avviata correttamente e il completamento verrà indicato in un secondo momento. |
| **OPERAZIONE WSA \_ \_ INTERROTTA** | L'operazione di I/O è stata interrotta a causa dell'uscita di un thread o di una richiesta dell'applicazione. Questo errore viene restituito se un'operazione sovrapposta è stata annullata a causa della chiusura del socket o **dell'SIO_FLUSH** comando IOCTL. |
| **WSAEACCES** | È stato effettuato un tentativo di accedere a un socket in modo non consentito dalle autorizzazioni di accesso. Questo errore viene restituito in diverse condizioni che includono le condizioni seguenti: l'utente non dispone dei privilegi amministrativi necessari nel computer locale o l'applicazione non è in esecuzione in una shell avanzata come amministratore predefinito ( `RunAs administrator` ). |
| **WSAEFAULT** | Il sistema ha rilevato un indirizzo puntatore non valido durante il tentativo di usare un argomento puntatore in una chiamata. Questo errore viene restituito dal parametro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *lpCompletionRoutine* non è completamente contenuto in una parte valida dello spazio indirizzi utente. |
| **WSAEINPROGRESS** | È in corso un'operazione di blocco. Questo errore viene restituito se la funzione viene richiamata quando è in corso un callback. |
| **WSAEINTR** | Un'operazione di blocco è stata interrotta da una chiamata a **WSACancelBlockingCall.** Questo errore viene restituito se un'operazione di blocco è stata interrotta. |
| **WSAEINVAL** | Argomento fornito non valido. Questo errore viene restituito se il *parametro dwIoControlCode* non è un comando valido o se un parametro di input specificato non è accettabile o il comando non è applicabile al tipo di socket specificato. |
| **WSAENETDOWN** | Rete inattiva rilevata durante l'operazione del socket. Questo errore viene restituito se il sottosistema di rete ha avuto esito negativo. |
| **Wsaenotsock** | È stata tentata un'operazione su un oggetto che non è un socket. Questo errore viene restituito se il descrittore *s* non è un socket. |
| **WSAEOPNOTSUPP** | L'operazione tentata non è supportata per il tipo di oggetto a cui si fa riferimento. Questo errore viene restituito se il comando IOCTL specificato non è supportato. Questo errore viene restituito anche se **SIO \_ SET WFP CONNECTION REDIRECT \_ \_ \_ \_ RECORDS** IOCTL non è supportato dal provider di trasporto. |

## <a name="remarks"></a>Commenti

**SIO \_ SET \_ WFP CONNECTION REDIRECT \_ \_ \_ RECORDS** IOCTL è supportato in Windows 8 e Windows Server 2012 e versioni successive del sistema operativo.

WFP consente l'accesso al percorso di elaborazione dei pacchetti TCP/IP, in cui i pacchetti in uscita e in ingresso possono essere esaminati o modificati prima di consentirne l'ulteriore elaborazione.
Sfruttando il percorso di elaborazione TCP/IP, i fornitori di software indipendenti (ISV) possono creare più facilmente firewall, software antivirus, software di diagnostica e altri tipi di applicazioni e servizi.
WFP fornisce componenti in modalità utente e kernel in modo che gli ISV di terze parti possano partecipare alle decisioni di filtro che si svolgono a più livelli nello stack del protocollo TCP/IP e in tutto il sistema operativo.
La funzionalità di reindirizzamento della connessione WFP consente a un driver kernel callout WFP di reindirizzare una connessione in locale a un processo in modalità utente, eseguire l'ispezione del contenuto in modalità utente e inoltrare il contenuto esaminato usando una connessione diversa alla destinazione originale.

**SIO \_ SET \_ WFP CONNECTION REDIRECT \_ \_ \_ RECORDS** IOCTL e diversi altri IOCTLS correlati sono componenti in modalità utente usati per consentire a più applicazioni proxy di connessione basate su WFP di controllare lo stesso flusso di traffico in modo cooperativo.
Ogni agente di ispezione può controllare nuovamente in modo sicuro il traffico di rete già controllato da un altro agente di ispezione.
Con la presenza di più proxy (sviluppati da ISV diversi, ad esempio), la connessione usata da un proxy per comunicare con la destinazione finale potrebbe a sua volta essere reindirizzata da un secondo proxy e tale nuova connessione potrebbe essere nuovamente reindirizzata dal proxy originale.
Senza il rilevamento delle connessioni, la connessione originale potrebbe non raggiungere mai la destinazione finale perché rimane bloccata in un ciclo di proxy infinito.

SIO **SET WFP CONNECTION REDIRECT \_ \_ \_ \_ \_ RECORDS** IOCTL viene usato per fornire il rilevamento delle connessioni proxy sulle connessioni socket reindirizzate.
Questa funzionalità WFP facilita il rilevamento dei record di reindirizzamento dal reindirizzamento iniziale di una connessione alla connessione finale alla destinazione.

[**L'ioCTL**](sio-query-wfp-connection-redirect-records.md) SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS viene usato da un servizio di reindirizzamento basato su WFP per recuperare il record di reindirizzamento dalla connessione di pacchetti TCP/IP accettata (ad esempio, il socket connesso per un socket TCP o un socket UDP) reindirizzato a esso dal callout in modalità kernel complementare registrato ai livelli **REDIRECT DI ALE \_ CONNECT \_** in un driver in modalità kernel.
Il [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) IOCTL recupera il contesto di reindirizzamento per un record di reindirizzamento, che viene usato.
Il contesto di reindirizzamento è facoltativo e viene usato se lo stato di reindirizzamento corrente di una connessione è che la connessione è stata reindirizzata dal servizio di reindirizzamento chiamante o che la connessione è stata reindirizzata in precedenza dal servizio di reindirizzamento chiamante, ma successivamente reindirizzata nuovamente da un altro servizio di reindirizzamento. Il servizio di reindirizzamento trasferisce il record di reindirizzamento recuperato al socket TCP che usa per eseguire il proxy del contenuto originale usando **SIO \_ SET WFP CONNECTION REDIRECT \_ \_ \_ \_ RECORDS** IOCTL.

L'applicazione che chiama **SIO \_ SET WFP CONNECTION REDIRECT \_ \_ \_ \_ RECORDS** IOCTL non deve comprendere il BLOB contenente il record di reindirizzamento impostato.
Si tratta di un BLOB opaco di dati che l'applicazione deve passare al nuovo socket.

## <a name="see-also"></a>Vedi anche

[**IPPROTO_IP Socket Options**](/windows/desktop/winsock/ipproto-ip-socket-options)

[**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md)

[**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md)

[**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**Wsaioctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
