---
description: Il codice di controllo applica una o più impostazioni di trasporto a un socket.
ms.assetid: FA0657EE-B65E-4EFA-AF1E-CA0EA7B27715
title: Codice di controllo SIO_APPLY_TRANSPORT_SETTING
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: e167a87e70dc3c6c44a263308beb333176a3d525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309933"
---
# <a name="sio_apply_transport_setting-control-code"></a>Codice di controllo SIO_APPLY_TRANSPORT_SETTING

## <a name="description"></a>Descrizione

Il codice di controllo **sio \_ Applica \_ trasporto \_** applica una o più impostazioni di trasporto a un socket.

Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_APPLY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to the output buffer
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_APPLY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to the output buffer
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
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
Usare **l' \_ \_ \_ impostazione applica trasporto sio** per questa operazione.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntatore al buffer di input.
Questo parametro contiene un puntatore a una struttura in cui il primo membro della struttura è una struttura [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) che determina quale impostazione di trasporto viene applicata.

### <a name="cbinbuffer"></a>cbInBuffer

Dimensione, in byte, del buffer di input.
Questo parametro dipende dall'impostazione di trasporto applicata.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntatore al buffer di output.
Questo parametro dipende dall'impostazione di trasporto applicata.

### <a name="cboutbuffer"></a>cbOutBuffer

Dimensione, in byte, del buffer di output.

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
| **\_operazione WSA \_ interrotta** | L'operazione di I/O è stata interrotta a causa dell'uscita di un thread o di una richiesta dell'applicazione. Questo errore viene restituito se un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del comando IOCTL di **\_ scaricamento sio** . |
| **WSAEFAULT** | Il sistema ha rilevato un indirizzo puntatore non valido durante il tentativo di usare un argomento puntatore in una chiamata. Questo errore viene restituito dal parametro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *il lpCompletionRoutine* non è interamente contenuto in una parte valida dello spazio degli indirizzi utente. |
| **WSAEINPROGRESS** | È in corso un'operazione di blocco. Questo errore viene restituito se la funzione viene richiamata quando è in corso un callback. |
| **WSAEINTR** | Un'operazione di blocco è stata interrotta da una chiamata a [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall). Questo errore viene restituito se un'operazione di blocco è stata interrotta. |
| **WSAEINVAL** | Argomento fornito non valido. Questo errore viene restituito se il parametro *dwIoControlCode* non è un comando valido o se un parametro di input specificato non è accettabile o se il comando non è applicabile al tipo di socket specificato. |
| **WSAENETDOWN** | Rete inattiva rilevata durante l'operazione del socket. Questo errore viene restituito se il sottosistema di rete non è riuscito. |
| **WSAENOTSOCK** | Si è tentato di eseguire un'operazione su un elemento che non è un socket. Questo errore viene restituito se il descrittore *s* non è un socket. |
| **ILWSAEOPNOTSUPP** | L'operazione tentata non è supportata per il tipo di oggetto a cui si fa riferimento. Questo errore viene restituito se il comando IOCTL specificato non è supportato. Questo errore viene restituito anche se l' **\_ impostazione applica \_ trasporto \_** IOCTL non è supportata dal provider di trasporto. Questo errore viene restituito anche quando viene eseguito un tentativo di usare l' **\_ impostazione del \_ trasporto \_ IOCTL Apply** per un socket diverso da UDP o TCP. |

## <a name="remarks"></a>Commenti

L' **\_ \_ \_ impostazione sio applica trasporto** IOCTL è supportata in windows 8 e Windows Server 2012 e versioni successive del sistema operativo.

L' **\_ \_ \_ impostazione sio applica trasporto** IOCTL è un IOCTL generico usato per applicare le impostazioni di trasporto al socket.
L'impostazione di trasporto da applicare è basata sul [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passato nel parametro *lpvInBuffer* .

A partire da Windows 8 e Windows Server 2012, il sistema definisce la funzionalità **REAL_TIME_NOTIFICATION_CAPABILITY** su un socket TCP.
A partire da Windows 10 e Windows Server 2016, viene definito anche il **\_ \_ contesto associato NAMERES** .
Per ulteriori informazioni, vedere [**addrinfoex4**](/windows/desktop/api/ws2def/ns-ws2def-addrinfoex4) e [**ASSOCIATE_NAMERES_CONTEXT_INPUT**](/windows/desktop/api/mstcpip/ns-mstcpip-associate_nameres_context_input).

Se il [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passato nel parametro lpvInBuffer ha il membro GUID impostato sulla **funzionalità di \_ \_ notifica in \_ tempo reale**, si tratta di una richiesta per applicare le impostazioni di notifica in tempo reale per il socket TCP usato con [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) per ricevere notifiche di rete in background in un'app di Windows Store.
Il parametro *lpvInBuffer* deve puntare a una struttura **REAL_TIME_NOTIFICATION_SETTING_INPUT** .
Il parametro *lpvOutBuffer* non è usato per questa operazione.
Questa impostazione del trasporto si applica solo ai socket TCP.
Questa impostazione del trasporto fornisce un modo per WinInet o servizi di rete simili per contrassegnare un socket TCP specificato come [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) abilitato.
Windows contrassegnerà il socket TCP corrispondente e configurerà le impostazioni hardware e software appropriate quando viene chiamata questa opzione.
Un'applicazione Windows Store non chiamerà direttamente questo IOCTL.

## <a name="see-also"></a>Vedi anche

[**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)

[presa](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**SIO_QUERY_TRANSPORT_SETTING**](sio-query-transport-setting.md)

[**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
