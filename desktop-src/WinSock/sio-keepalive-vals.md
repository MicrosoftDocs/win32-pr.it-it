---
description: Il codice di controllo Abilita o Disabilita l'impostazione per connessione dell'opzione keep-alive TCP che specifica il timeout e l'intervallo keep-alive TCP.
ms.assetid: c02e8ad5-bfad-489f-83bf-39b53fd68bde
title: Codice di controllo SIO_KEEPALIVE_VALS
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ea8aabf452436ca2bbd6307366e7fc24f913dbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131019"
---
# <a name="sio_keepalive_vals-control-code"></a>Codice di controllo SIO_KEEPALIVE_VALS

## <a name="description"></a>Descrizione

Il codice di controllo **sio \_ KeepAlive \_ Vals** Abilita o Disabilita l'impostazione per connessione dell'opzione keep-alive TCP che specifica il timeout e l'intervallo keep-alive TCP.

Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.

```cpp
int WSAIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
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
Per questa operazione, usare **sio \_ KeepAlive \_** per questa operazione.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntatore al buffer di input.
Questo parametro deve puntare a una struttura **TCP \_ KeepAlive** .

### <a name="cbinbuffer"></a>cbInBuffer

Dimensione, in byte, del buffer di input.
Questo parametro deve essere uguale o maggiore della dimensione della struttura **TCP \_ KeepAlive** a cui punta il parametro *lpvInBuffer* .

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
|**\_io WSA \_ in sospeso** | Un'operazione sovrapposta è stata avviata correttamente e il completamento verrà indicato in un secondo momento. |
| **\_operazione WSA \_ interrotta** | Un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del comando **IOCTL SIO_FLUSH** . |
| **WSAEFAULT** | Il parametro *lpOverlapped* o *il lpCompletionRoutine* non è interamente contenuto in una parte valida dello spazio degli indirizzi utente. |
| **WSAEINPROGRESS** | La funzione viene richiamata quando è in corso un callback. |
| **WSAEINTR** | Un'operazione di blocco è stata interrotta. |
| **WSAEINVAL** | Il parametro *dwIoControlCode* non è un comando valido oppure un parametro di input specificato non è accettabile oppure il comando non è applicabile al tipo di socket specificato. |
| **WSAENETDOWN** | Il sottosistema di rete non è riuscito. |
| **WSAENOPROTOOPT** | L'opzione socket non è supportata nel protocollo specificato. Questo errore viene restituito per un socket di datagramma. |
| **WSAENOTSOCK** | Il descrittore s non è un socket. |
| **ILWSAEOPNOTSUPP** | Il comando IOCTL specificato non è supportato. Questo errore viene restituito se il provider di trasporto non supporta il IOCTL di **sio \_ KeepAlive \_** . |

## <a name="remarks"></a>Commenti

Il IOCTL di **sio \_ KeepAlive \_ Vals** è supportato in Windows 2000 e versioni successive del sistema operativo.

Il codice di controllo **sio \_ KeepAlive \_ Vals** Abilita o Disabilita l'impostazione per connessione dell'opzione keep-alive TCP che specifica il timeout e l'intervallo keep-alive TCP utilizzati per i pacchetti keep-alive TCP.
Per ulteriori informazioni sull'opzione Keep-Alive, vedere la sezione 4.2.3.6 in requisiti per gli host Internet-livelli di comunicazione specificati in RFC 1122 disponibili sul [sito Web IETF](https://www.ietf.org/rfc/rfc1122.txt).
Questa risorsa può essere disponibile solo in inglese.

Il parametro *lpvInBuffer* deve puntare a una struttura **TCP \_ KeepAlive** definita nel file di intestazione *MSTCPIP. h* .
Questa struttura viene definita nel modo seguente:

```cpp
/* Argument structure for SIO_KEEPALIVE_VALS */
struct tcp_keepalive {
    u_long  onoff;
    u_long  keepalivetime;
    u_long  keepaliveinterval;
};
```

Il valore specificato nel membro **OnOff** determina se il keep-alive TCP è abilitato o disabilitato.
Se il membro **OnOff** è impostato su un valore diverso da zero, viene abilitato TCP Keep-Alive e vengono utilizzati gli altri membri della struttura.
Il membro **KeepAliveTime** specifica il timeout, in millisecondi, senza alcuna attività fino a quando non viene inviato il primo pacchetto keep-alive.
Il membro **keepAliveInterval** specifica l'intervallo in millisecondi tra l'invio di pacchetti keep-alive successivi in caso di ricezione di un riconoscimento.

L'opzione [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) , che corrisponde a una delle [**Opzioni di SOL_SOCKET Socket**](/windows/desktop/winsock/sol-socket-socket-options), può essere usata anche per abilitare o disabilitare il keep-alive TCP in una connessione, nonché per eseguire query sullo stato corrente di questa opzione.
Per eseguire una query sul fatto che il keep-alive TCP sia abilitato in un socket, è possibile chiamare la funzione getsockopt con l'opzione [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) .
Per abilitare o disabilitare il keep-alive TCP, è possibile chiamare la funzione **setsockopt** con l'opzione [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) .
Se il keep-alive TCP è abilitato con [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive), le impostazioni TCP predefinite vengono usate per il timeout e l'intervallo keep-alive, a meno che tali valori non siano stati modificati usando **sio \_ KeepAlive \_ Vals**.

Il valore predefinito a livello di sistema del timeout keep-alive è controllabile tramite l'impostazione del registro di sistema [**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) che accetta un valore in millisecondi. Se la chiave non è impostata, il timeout keep-alive predefinito è 2 ore.
Il valore predefinito a livello di sistema dell'intervallo keep-alive è controllabile tramite l'impostazione del registro di sistema [**keepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) che accetta un valore in millisecondi. Se la chiave non è impostata, l'intervallo keep-alive predefinito è di 1 secondo.

In Windows Vista e versioni successive, il numero di probe Keep-Alive (ritrasmissioni dati) è impostato su 10 e non può essere modificato.

In Windows Server 2003, Windows XP e Windows 2000, l'impostazione predefinita per numero di probe Keep-Alive è 5.
Il numero di probe Keep-Alive è controllabile tramite le impostazioni del registro di sistema **TcpMaxDataRetransmissions** e [**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) .
Il numero di probe Keep-Alive è impostato sul valore più elevato tra i due valori della chiave del registro di sistema.
Se questo numero è 0, i probe Keep-Alive non verranno inviati.
Se questo numero è superiore a 255, viene impostato su 255.

## <a name="see-also"></a>Vedi anche

[**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))

[**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))

[**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))

[presa](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
