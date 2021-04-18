---
description: Il codice di controllo ottiene un elenco degli indirizzi di trasporto locali della famiglia di protocolli del socket a cui l'applicazione può eseguire il binding.
ms.assetid: 6b23a019-812c-4623-941b-87928acabbd2
title: Codice di controllo SIO_ADDRESS_LIST_QUERY
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 7a728293afa51ceb58d61141e7184077478b787c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315788"
---
# <a name="sio_address_list_query-control-code"></a>Codice di controllo SIO_ADDRESS_LIST_QUERY

## <a name="description"></a>Descrizione

Il codice di controllo della **\_ query dell' \_ elenco \_ di indirizzi sio** ottiene un elenco degli indirizzi di trasporto locali della famiglia di protocolli del socket a cui l'applicazione può eseguire il binding.
L'elenco di indirizzi varia in base alla famiglia di indirizzi e alcuni indirizzi sono esclusi dall'elenco.

Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
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
Usare **la \_ \_ \_ query dell'elenco di indirizzi sio** per questa operazione.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntatore al buffer di input.
Questo parametro non è utilizzato per questa operazione.

### <a name="cbinbuffer"></a>cbInBuffer

Dimensione, in byte, del buffer di input.
Questo parametro non è utilizzato per questa operazione.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntatore al buffer di output.

### <a name="cboutbuffer"></a>cbOutBuffer

Dimensione, in byte, del buffer di output.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Puntatore a una variabile che riceve le dimensioni, in byte, dei dati archiviati nel buffer di output.

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
| **WSAEINVAL** | Il parametro *dwIoControlCode* non è un comando valido oppure un parametro di input specificato non è accettabile oppure il comando non è applicabile al tipo di socket specificato. Questo errore viene restituito se il parametro *cbInBuffer* non è impostato su **null**. |
| **WSAENETDOWN** | Il sottosistema di rete non è riuscito. |
| **WSAENOBUFS** | Non è disponibile spazio nel buffer. |
| **WSAENOPROTOOPT** | L'opzione socket non è supportata nel protocollo specificato. |
| **WSAENOTSOCK** | Il descrittore *s* non è un socket. |
| **ILWSAEOPNOTSUPP** | Il comando IOCTL specificato non è supportato. Questo errore viene restituito se la **\_ query dell' \_ elenco \_ di indirizzi sio** non è supportata dal provider di trasporto. |

## <a name="remarks"></a>Commenti

La **\_ \_ \_ query elenco indirizzi sio** è supportata in Windows 2000 e versioni successive del sistema operativo.

Il codice di controllo della **\_ query dell' \_ elenco \_ di indirizzi sio** ottiene un elenco degli indirizzi di trasporto locali della famiglia di protocolli del socket a cui l'applicazione può eseguire il binding.
L'elenco di indirizzi varia in base alla famiglia di indirizzi.

Per la \_ famiglia di indirizzi AF INET6, vengono restituiti tutti gli indirizzi tranne i seguenti:

* Qualsiasi indirizzo IP in cui lo stato di rilevamento degli indirizzi duplicati (DAD) non è IpDadStatePreferred.
* Qualsiasi indirizzo IP con un livello di ambito inferiore a ScopeLevelSubnet su un'interfaccia in cui il tipo di interfaccia è **se \_ digitare \_ \_ loopback software**.
Questo significa che gli indirizzi locali di collegamento (FE80: *) e loopback (:: 1) sulle interfacce di se il tipo di **\_ \_ \_ loopback software** sono esclusi, ma non se questi indirizzi si trovano su un'interfaccia con un tipo diverso.

Per la famiglia di indirizzi **AF \_ inet** , vengono restituiti tutti gli indirizzi tranne i seguenti:

* Qualsiasi indirizzo IP in cui lo stato di rilevamento degli indirizzi duplicati (DAD) non è IpDadStatePreferred.
* Qualsiasi indirizzo IP in un'interfaccia in cui il tipo di interfaccia è **se il \_ tipo di \_ \_ loopback** e il collegamento del software sono locali.
Questo significa che gli indirizzi locali rispetto al collegamento (169,254.*) e loopback (127.*) sulle interfacce di se il tipo di **\_ \_ \_ loopback software** è escluso, ma non se questi indirizzi si trovano su un'interfaccia con un tipo diverso.

Per ulteriori informazioni sullo stato di DAD, vedere la documentazione dell'helper IP sull' [**enumerazione \_ \_ dello stato IP DAD**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state) e la struttura degli [**\_ \_ \_ indirizzi unicast dell'adapter IP**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh) e la documentazione MIB sulla struttura di [**\_ \_ riga MIB UNICASTIPADDRESS**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row) .
Per ulteriori informazioni sul tipo di interfaccia, vedere la documentazione dell'helper IP sulla struttura degli [**\_ \_ indirizzi IP dell'adapter**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) e la funzione [**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) e la documentazione MIB in [**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2) struttura.
Per ulteriori informazioni sul livello di ambito, vedere la documentazione dell'helper IP sulla struttura [**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) e l'enumerazione [**a \_ livello di ambito**](/windows/desktop/api/ws2def/ne-ws2def-scope_level) .

L'elenco restituito nel buffer di output a cui fa riferimento il parametro *lpvOutBuffer* è nel formato di una struttura dell' [**elenco di \_ indirizzi \_ del socket**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list) .

Se il buffer di output specificato nel parametro *lpvOutBuffer* non è sufficientemente grande da contenere l'elenco indirizzi, viene restituito un **\_ errore socket** come risultato di questo IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [WSAEFAULT](windows-sockets-error-codes-2.md).
La dimensione richiesta, in byte, per il buffer di output viene restituita nel parametro *lpcbBytesReturned* in questo caso.
Si noti che il codice di errore [WSAEFAULT](windows-sockets-error-codes-2.md) viene restituito anche se il parametro *lpvInBuffer*, *lpvOutBuffer* o *lpcbBytesReturned* non è completamente contenuto in una parte valida dello spazio degli indirizzi utente.

La **\_ query di \_ elenco \_ indirizzi sio** viene in genere chiamata in modo sincrono con il parametro *lpvOverlapped* impostato su **null**, perché l'elenco di indirizzi viene restituito immediatamente.

**Nota**  Negli ambienti plug-n-Play di Windows gli indirizzi possono essere aggiunti e rimossi dinamicamente.
Pertanto, le applicazioni non possono basarsi sulle informazioni restituite dalla **\_ query dell' \_ elenco \_ di indirizzi sio** per essere persistenti.
Le applicazioni possono registrarsi per le notifiche di modifica degli indirizzi tramite l' **\_ elenco indirizzi sio \_ \_ modificare** IOCTL, che fornisce la notifica tramite l'evento di **\_ \_ \_ modifica elenco indirizzi** I/o sovrapposto o FD.
La sequenza di azioni seguente può essere utilizzata per garantire che l'applicazione disponga sempre di informazioni sull'elenco di indirizzi correnti:

* Rilasciare l' **\_ elenco indirizzi \_ sio \_ modificare** IOCTL
* Eseguire la **\_ query dell' \_ elenco \_ di indirizzi sio**
* Ogni volta che l' **\_ elenco di indirizzi sio \_ \_ modifica** la chiamata IOCTL, informa l'applicazione di una modifica dell'elenco di indirizzi (tramite i/o sovrapposti o segnalando l'evento di modifica dell' **\_ \_ elenco \_ di indirizzi FD** ), l'intera sequenza di azioni deve essere ripetuta.

In Microsoft Windows Software Development Kit (SDK) rilasciato per Windows Vista e versioni successive, l'organizzazione dei file di intestazione è stata modificata e il codice di controllo della **\_ query dell' \_ elenco \_ di indirizzi sio** è definito nel file di intestazione *Ws2def. h* .
Si noti che il file di intestazione *Ws2def. h* viene incluso automaticamente in *Winsock2. h* e non deve mai essere utilizzato direttamente.

## <a name="see-also"></a>Vedi anche

[**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

[**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp)

[**IP_ADAPTER_UNICAST_ADDRESS**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh)

[**IP_DAD_STATE**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state)

[**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2)

[**MIB_UNICASTIPADDRESS_ROW**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row)

[**SCOPE_LEVEL**](/windows/desktop/api/ws2def/ne-ws2def-scope_level)

[**SOCKET_ADDRESS_LIST**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list)

[**presa**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
