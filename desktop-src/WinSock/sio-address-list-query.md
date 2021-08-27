---
description: Il codice di controllo ottiene un elenco di indirizzi di trasporto locali della famiglia di protocolli del socket a cui l'applicazione può eseguire l'associazione.
ms.assetid: 6b23a019-812c-4623-941b-87928acabbd2
title: SIO_ADDRESS_LIST_QUERY di controllo
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 57d529ed4ea525b01e294efcacc1aa8dd2b118106177bd46cb64ffdf42a31a58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097531"
---
# <a name="sio_address_list_query-control-code"></a>SIO_ADDRESS_LIST_QUERY di controllo

## <a name="description"></a>Descrizione

Il **codice di controllo \_ \_ \_ SIO ADDRESS LIST QUERY** ottiene un elenco di indirizzi di trasporto locali della famiglia di protocolli del socket a cui l'applicazione può eseguire l'associazione.
L'elenco di indirizzi varia in base alla famiglia di indirizzi e alcuni indirizzi vengono esclusi dall'elenco.

Per eseguire questa operazione, chiamare [**la funzione WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.

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
Usare **SIO \_ ADDRESS LIST \_ \_ QUERY** per questa operazione.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntatore al buffer di input.
Questo parametro non è usato per questa operazione.

### <a name="cbinbuffer"></a>cbInBuffer

Dimensione, in byte, del buffer di input.
Questo parametro non è usato per questa operazione.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntatore al buffer di output.

### <a name="cboutbuffer"></a>cbOutBuffer

Dimensione, in byte, del buffer di output.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Puntatore a una variabile che riceve le dimensioni, in byte, dei dati archiviati nel buffer di output.

### <a name="lpvoverlapped"></a>lpvOverlapped

Puntatore a una [**struttura WSAOVERLAPPED.**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

Se i socket *sono* stati creati senza l'attributo sovrapposto, il *parametro lpOverlapped* viene ignorato.

Se *s è* stato aperto con l'attributo sovrapposto e il parametro *lpOverlapped* non è **NULL,** l'operazione viene eseguita come operazione sovrapposta (asincrona).
In questo caso, *il parametro lpOverlapped* deve puntare a una [**struttura WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valida.

Per le operazioni sovrapposte, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce immediatamente un risultato e il metodo di completamento appropriato viene segnalato quando l'operazione è stata completata.
In caso contrario, la funzione non restituisce un valore finché l'operazione non viene completata o non si verifica un errore.

### <a name="lpcompletionroutine"></a>lpCompletionRoutine

Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)

Puntatore alla routine di completamento chiamata quando l'operazione è stata completata (ignorata per i socket non sovrapposti).

### <a name="lpthreadid"></a>lpThreadId

Puntatore a una [**struttura WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) che deve essere utilizzata dal provider in una chiamata successiva a [**WPUQueueApc.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)
Il provider deve archiviare la struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a cui si fa riferimento (non il puntatore allo stesso) fino al termine della [**funzione WPUQueueApc.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)

**Nota**  Questo parametro si applica solo alla **funzione WSPIoctl.**

### <a name="lperrno"></a>lpErrno

Puntatore al codice di errore.

**Nota**  Questo parametro si applica solo alla **funzione WSPIoctl.**

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, la [**funzione WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce zero.

Se l'operazione non riesce o è in sospeso, la [**funzione WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce **SOCKET \_ ERROR**.
Per ottenere informazioni estese sull'errore, [**chiamare WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).

| Codice di errore | Significato |
|------------|---------|
| **I/O WSA \_ \_ IN SOSPESO** | Un'operazione sovrapposta è stata avviata correttamente e il completamento verrà indicato in un secondo momento. |
| **OPERAZIONE WSA \_ \_ INTERROTTA** | Un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del **comando SIO \_ FLUSH** IOCTL. |
| **WSAEFAULT** | Il *parametro lpOverlapped* o *lpCompletionRoutine* non è completamente contenuto in una parte valida dello spazio degli indirizzi utente. |
| **WSAEINPROGRESS** | La funzione viene richiamata quando è in corso un callback. |
| **WSAEINTR** | Un'operazione di blocco è stata interrotta. |
| **WSAEINVAL** | Il *parametro dwIoControlCode* non è un comando valido o un parametro di input specificato non è accettabile oppure il comando non è applicabile al tipo di socket specificato. Questo errore viene restituito se il *parametro cbInBuffer* non è impostato su **NULL.** |
| **WSAENETDOWN** | Errore del sottosistema di rete. |
| **WSAENOBUFS** | Non è disponibile spazio nel buffer. |
| **WSAENOPROTOOPT** | L'opzione socket non è supportata nel protocollo specificato. |
| **Wsaenotsock** | Il descrittore *s* non è un socket. |
| **WSAEOPNOTSUPP** | Il comando IOCTL specificato non è supportato. Questo errore viene restituito se **SIO \_ ADDRESS LIST \_ \_ QUERY** IOCTL non è supportato dal provider di trasporto. |

## <a name="remarks"></a>Commenti

**SIO \_ ADDRESS \_ LIST \_ QUERY** IOCTL è supportato in Windows 2000 e versioni successive del sistema operativo.

Il **codice di controllo \_ \_ \_ SIO ADDRESS LIST QUERY** ottiene un elenco di indirizzi di trasporto locali della famiglia di protocolli del socket a cui l'applicazione può eseguire l'associazione.
L'elenco di indirizzi varia in base alla famiglia di indirizzi.

Per la famiglia \_ di indirizzi AF INET6, vengono restituiti tutti gli indirizzi ad eccezione dei seguenti:

* Qualsiasi indirizzo IP in cui lo stato di rilevamento degli indirizzi duplicati non è IpDadStatePreferred.
* Qualsiasi indirizzo IP con un livello di ambito inferiore a ScopeLevelSubnet in un'interfaccia in cui il tipo di interfaccia è **IF \_ TYPE SOFTWARE \_ \_ LOOPBACK**.
Ciò significa che gli indirizzi locali di collegamento (fe80:*) e di loopback (::1) nelle interfacce di tipo **IF \_ TYPE SOFTWARE \_ \_ LOOPBACK** vengono esclusi, ma non se questi indirizzi si verificano in un'interfaccia di tipo diverso.

Per la **famiglia di indirizzi AF \_ INET,** vengono restituiti tutti gli indirizzi ad eccezione dei seguenti:

* Qualsiasi indirizzo IP in cui lo stato di rilevamento degli indirizzi duplicati non è IpDadStatePreferred.
* Qualsiasi indirizzo IP in un'interfaccia in cui il tipo di interfaccia è **IF \_ TYPE SOFTWARE \_ \_ LOOPBACK** e il collegamento è locale.
Ciò significa che gli indirizzi link-local (169.254. ) e *loopback (127.*) sulle interfacce di tipo **IF TYPE SOFTWARE \_ \_ \_ LOOPBACK** sono esclusi, ma non se questi indirizzi si verificano in un'interfaccia di tipo diverso.

Per altre informazioni sullo stato DELL'helper IP, vedere la documentazione relativa all'enumerazione [**\_ \_ IPSTATUS**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state) e alla struttura IP [**ADAPTER \_ \_ UNICAST \_ ADDRESS**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh) e la documentazione MIB sulla struttura [**MIB \_ UNICASTIPADDRESS \_ ROW.**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row)
Per altre informazioni sul tipo di interfaccia, vedere la documentazione dell'helper IP sulla struttura [**IP \_ ADAPTER \_ ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) e la funzione [**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) e la documentazione MIB [**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2) struttura.
Per altre informazioni sul livello di ambito, vedere la documentazione dell'helper IP [**sulla struttura**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) IP_ADAPTER_ADDRESSES e sull'enumerazione [**SCOPE \_ LEVEL.**](/windows/desktop/api/ws2def/ne-ws2def-scope_level)

L'elenco restituito nel buffer di output a cui punta *il parametro lpvOutBuffer* è nel formato di una [**struttura SOCKET ADDRESS \_ \_ LIST.**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list)

Se il buffer di output specificato nel parametro *lpvOutBuffer* non è sufficientemente grande da contenere l'elenco di indirizzi, viene restituito **SOCKET \_ ERROR** come risultato di questo IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [WSAEFAULT.](windows-sockets-error-codes-2.md)
In questo caso, le dimensioni richieste, in byte, per il buffer di output vengono restituite nel parametro *lpcbBytesReturned.*
Si noti che il codice di errore [WSAEFAULT](windows-sockets-error-codes-2.md) viene restituito anche se il parametro *lpvInBuffer*, *lpvOutBuffer* o *lpcbBytesReturned* non è completamente contenuto in una parte valida dello spazio degli indirizzi utente.

LA **QUERY SIO \_ ADDRESS LIST \_ \_ IOCTL** viene in genere chiamata in modo sincrono con il parametro *lpvOverlapped* impostato su **NULL,** poiché l'elenco di indirizzi viene restituito immediatamente.

**Nota**  In Windows plug-n-play, gli indirizzi possono essere aggiunti e rimossi in modo dinamico.
Pertanto, le applicazioni non possono basarsi sulle informazioni restituite da **SIO \_ ADDRESS LIST \_ \_ QUERY** per essere persistenti.
Le applicazioni possono registrarsi per le notifiche di modifica degli indirizzi tramite l'IOCTL **SIO \_ ADDRESS LIST \_ \_ CHANGE,** che fornisce la notifica tramite l'evento di I/O sovrapposto o **FD ADDRESS LIST \_ \_ \_ CHANGE.**
La sequenza di azioni seguente può essere usata per garantire che l'applicazione abbia sempre informazioni aggiornate sull'elenco di indirizzi:

* Eseguire **l'IOCTL SIO \_ ADDRESS \_ LIST \_ CHANGE**
* Eseguire LA **QUERY SIO \_ ADDRESS \_ LIST \_** IOCTL
* Ogni volta che la chiamata **SIO \_ ADDRESS LIST \_ \_ CHANGE** IOCTL notifica all'applicazione una modifica dell'elenco di indirizzi (tramite I/O sovrapposto o segnalando l'evento **FD ADDRESS LIST \_ \_ \_ CHANGE),** l'intera sequenza di azioni deve essere ripetuta.

In Microsoft Windows Software Development Kit (SDK) rilasciato per Windows Vista e versioni successive, l'organizzazione dei file di intestazione è stata modificata e il codice di controllo **\_ \_ \_ SIO ADDRESS LIST QUERY** è definito nel file di intestazione *Ws2def.h.*
Si noti che il file di intestazione *Ws2def.h* viene incluso automaticamente in *Winsock2.h* e non deve mai essere usato direttamente.

## <a name="see-also"></a>Vedi anche

[**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

[**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp)

[**IP_ADAPTER_UNICAST_ADDRESS**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh)

[**IP_DAD_STATE**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state)

[**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2)

[**MIB_UNICASTIPADDRESS_ROW**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row)

[**SCOPE_LEVEL**](/windows/desktop/api/ws2def/ne-ws2def-scope_level)

[**SOCKET_ADDRESS_LIST**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list)

[**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**Wsaioctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
