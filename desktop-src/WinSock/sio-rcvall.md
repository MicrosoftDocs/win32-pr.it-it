---
description: Il codice di controllo consente a un socket di ricevere tutti i pacchetti IPv4 o IPv6 che passano attraverso un'interfaccia di rete.
ms.assetid: 1c198a70-6669-4599-bd9a-ffc26c9fe1d0
title: Codice di controllo SIO_RCVALL
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ddff631f1fa4b6b9f9af74f71e2b1eb38a2bf48e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306903"
---
# <a name="sio_rcvall-control-code"></a>Codice di controllo SIO_RCVALL

## <a name="description"></a>Descrizione
Il codice di controllo **sio \_ RCVALL** consente a un socket di ricevere tutti i pacchetti IPv4 o IPv6 che passano attraverso un'interfaccia di rete.

Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_RCV_ALL,                       // dwIoControlCode
  NULL,                              // lpvInBuffer0,                                 // cbInBuffer
  NULL,                              // lpvOutBuffer output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_RCV_ALL,                       // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  NULL,                              // lpvOutBuffer output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

## <a name="parameters"></a>Parametri

### <a name="s"></a>s

Descrittore che identifica un socket.

### <a name="dwiocontrolcode"></a>dwIoControlCode

Codice di controllo per l'operazione.
Usare **sio \_ RCVALL** per questa operazione.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntatore al buffer di input che deve contenere il valore dell'opzione.
I valori possibili per l'opzione IOCTL **\_ RCVALL di sio** sono specificati nell'enumerazione **RCVALL_VALUE** definita nel file di intestazione *MSTCPIP. h* .

I valori possibili per **sio \_ RCVALL** sono i seguenti:

| Valore | Significato |
|-------|---------|
| **RCVALL \_ disattivato** | Disabilitare questa opzione in modo che un socket non riceva tutti i pacchetti IPv4 o IPv6 che passano attraverso un'interfaccia di rete. |
| **RCVALL \_** | Abilitare questa opzione per consentire a un socket di ricevere tutti i pacchetti IPv4 o IPv6 che passano attraverso un'interfaccia di rete. Questa opzione Abilita la modalità promiscua sulla scheda di interfaccia di rete (NIC) se la scheda di interfaccia di rete supporta la modalità promiscua. In un segmento LAN con un hub di rete, una scheda di interfaccia di rete che supporta la modalità promiscua acquisisce tutto il traffico IPv4 o IPv6 sulla LAN, incluso il traffico tra altri computer nello stesso segmento LAN. Tutti i pacchetti acquisiti (IPv4 o IPv6, a seconda del socket) verranno recapitati al socket non elaborato. Questa opzione non consente di acquisire altri pacchetti (ad esempio, i pacchetti ARP, IPX e NetBEUI) nell'interfaccia. Netmon usa la stessa modalità per l'interfaccia di rete, ma non usa questa opzione per acquisire il traffico. |
| **\_SOCKETLEVELONLY RCVALL** | Questa funzionalità non è attualmente implementata, pertanto l'impostazione di questa opzione non ha alcun effetto. |
| **\_IPLEVEL RCVALL** | Abilitare questa opzione per consentire a un socket IPv4 o IPv6 di ricevere tutti i pacchetti a livello IP che passano attraverso un'interfaccia di rete. Questa opzione non Abilita la modalità promiscua nella scheda di interfaccia di rete. Questa opzione influiscono solo sull'elaborazione dei pacchetti a livello IP. La scheda di interfaccia di rete riceve ancora solo i pacchetti indirizzati agli indirizzi unicast e multicast configurati. Tuttavia, un socket con questa opzione abilitata riceverà non solo i pacchetti diretti a indirizzi IP specifici, ma riceverà tutti i pacchetti IPv4 o IPv6 ricevuti dalla scheda di interfaccia di rete. Questa opzione non consente di acquisire altri pacchetti (ad esempio, i pacchetti ARP, IPX e NetBEUI) ricevuti sull'interfaccia. |

### <a name="cbinbuffer"></a>cbInBuffer

Dimensione, in byte, del buffer di input.
Questo parametro deve essere uguale o maggiore della dimensione del **RCVALL_VALUE** valore di enumerazione a cui punta il parametro *lpvInBuffer* .

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntatore al buffer di output.
Questo parametro non è utilizzato per questa operazione.

### <a name="cboutbuffer"></a>cbOutBuffer

Dimensione, in byte, del buffer di output.
Questo parametro non è utilizzato per questa operazione.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Puntatore a una variabile che riceve le dimensioni, in byte, dei dati archiviati nel buffer di output.
Questo parametro non è utilizzato per questa operazione.

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
| **\_operazione WSA \_ interrotta** | Un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del comando IOCTL **SIO_FLUSH** . |
| **WSAEFAULT** | Il parametro *lpOverlapped* o *il lpCompletionRoutine* non è interamente contenuto in una parte valida dello spazio degli indirizzi utente. |
| **WSAEINPROGRESS** | La funzione viene richiamata quando è in corso un callback. |
| **WSAEINTR** | Un'operazione di blocco è stata interrotta. |
| **WSAEINVAL** | Il parametro *dwIoControlCode* non è un comando valido oppure un parametro di input specificato non è accettabile oppure il comando non è applicabile al tipo di socket specificato. Questo errore viene restituito anche se il parametro *cbInBuffer* è minore di `sizeof(UCHAR)` o il parametro *lpvInBuffer* punta a un valore che non è un valore di enumerazione **RCVALL_VALUE** . Questo errore può essere restituito anche se non è possibile trovare l'interfaccia di rete associata al socket. Questo problema può verificarsi se l'interfaccia di rete associata al socket viene eliminata o rimossa (ad esempio, un dispositivo di rete USB Remove PCMCIA o USB). |
| **WSAENETDOWN** | Il sottosistema di rete non è riuscito. |
| **WSAENOBUFS** | Non è disponibile spazio nel buffer. |
| **WSAENOPROTOOPT** | L'opzione socket non è supportata nel protocollo specificato. |
| **WSAENOTSOCK** | Il descrittore *s* non è un socket. |
| **ILWSAEOPNOTSUPP** | Il comando IOCTL specificato non è supportato. Questo errore viene restituito se l' **IOCTL \_ RCVALL di sio** non è supportato dal provider di trasporto. |

## <a name="remarks"></a>Commenti

L' **IOCTL \_ RCVALL sio** è supportato in Windows 2000 e versioni successive del sistema operativo.

L' **IOCTL \_ RCVALL di sio** consente a un socket di ricevere tutti i pacchetti IPv4 o IPv6 in un'interfaccia di rete.
L'handle del socket passato alla funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** deve essere uno dei seguenti:

* Un socket IPv4 creato con la famiglia di indirizzi impostata su AF_INET, il tipo di socket impostato su SOCK_RAW e il protocollo impostato su IPPROTO_IP.
* Socket IPv6 creato con la famiglia di indirizzi impostata su AF_INET6, il tipo di socket impostato su SOCK_RAW e il protocollo impostato su IPPROTO_IPV6.

Per ulteriori informazioni sui socket non elaborati, vedere [**TCP/IP raw Sockets**](/windows/desktop/winsock/tcp-ip-raw-sockets-2).

Il socket deve anche essere associato a un'interfaccia IPv4 o IPv6 locale esplicita, il che significa che non è possibile eseguire l'associazione a **inaddr \_ any** o **in6addr \_ any**.

Una volta che il socket è stato associato e l'IOCTL viene completato correttamente, le chiamate alle funzioni [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv) o [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv) restituiscono datagrammi IPv4 che passano attraverso l'interfaccia IPv4 specificata o restituiscono datagrammi IPv6 passando attraverso l'interfaccia IPv6 specificata.
Si noti che è necessario fornire un buffer sufficientemente grande.
Impostando questo IOCTL, i pacchetti IPv4 o IPv6 vengono acquisiti solo su una determinata interfaccia.
Questo IOCTL non acquisisce altri pacchetti (ad esempio, i pacchetti ARP, IPX e NetBEUI) nell'interfaccia.

Un socket associato a una specifica interfaccia locale con l' **IOCTL \_ RCVALL di sio** riceverà solo i pacchetti che passano attraverso tale interfaccia.
Non riceverà i pacchetti ricevuti su un'altra interfaccia e verrà inoltrato a un'altra interfaccia diversa da quella associata al socket **sio \_ RCVALL** .

In Windows Server 2008 e versioni precedenti, l'impostazione IOCTL **\_ RCVALL di sio** non acquisisce i pacchetti locali inviati da un'interfaccia di rete.
Sono stati inclusi i pacchetti ricevuti su un'altra interfaccia ed è stata inoltrata l'interfaccia di rete specificata per l'IOCTL **\_ RCVALL sio** .

In Windows 7 e Windows Server 2008 R2 questa operazione è stata modificata in modo da acquisire anche i pacchetti locali inviati da un'interfaccia di rete.
Sono inclusi i pacchetti ricevuti su un'altra interfaccia e quindi l'interfaccia di rete associata al socket con IOCTL **\_ RCVALL di sio** .

Per impostare questo IOCTL è necessario disporre dei privilegi di amministratore nel computer locale.

Questa funzionalità viene talvolta definita modalità promiscua.
Qualsiasi modifica diretta rispetto all'applicazione di questa opzione su un'interfaccia e quindi a un'altra interfaccia con una singola chiamata che usa questo IOCTL non è supportata.
Un'applicazione deve innanzitutto utilizzare questo IOCTL per disattivare il comportamento sulla prima interfaccia e quindi utilizzare questo IOCTL per abilitare il comportamento su una nuova interfaccia.

## <a name="see-also"></a>Vedi anche

[**presa**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**Socket TCP/IP raw**](/windows/desktop/winsock/tcp-ip-raw-sockets-2)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
