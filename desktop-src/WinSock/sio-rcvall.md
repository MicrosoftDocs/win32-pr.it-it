---
description: Il codice di controllo consente a un socket di ricevere tutti i pacchetti IPv4 o IPv6 che passano attraverso un'interfaccia di rete.
ms.assetid: 1c198a70-6669-4599-bd9a-ffc26c9fe1d0
title: SIO_RCVALL codice di controllo
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: d545bcdf8f3cc01159b3afbc86a686fb2bf8e83493784d2197353f19ff01e576
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993431"
---
# <a name="sio_rcvall-control-code"></a>SIO_RCVALL codice di controllo

## <a name="description"></a>Descrizione
Il **codice di controllo SIO \_ RCNTASSI** consente a un socket di ricevere tutti i pacchetti IPv4 o IPv6 che passano attraverso un'interfaccia di rete.

Per eseguire questa operazione, chiamare [**la funzione WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.

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
Usare **SIO \_ RCACCI** per questa operazione.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntatore al buffer di input che deve contenere il valore dell'opzione.
I valori possibili per l'opzione **SIO \_ RC RPC** IOCTL sono specificati nell'enumerazione **RCVALL_VALUE** definita nel file di intestazione *Mstcpip.h.*

I valori possibili per **SIO \_ RCNTASSI** sono i seguenti:

| Valore | Significato |
|-------|---------|
| **RC RPC \_ OFF** | Disabilitare questa opzione in modo che un socket non riceva tutti i pacchetti IPv4 o IPv6 che passano attraverso un'interfaccia di rete. |
| **RC RPC \_ ON** | Abilitare questa opzione in modo che un socket riceva tutti i pacchetti IPv4 o IPv6 che passano attraverso un'interfaccia di rete. Questa opzione abilita la modalità promiscua nella scheda di interfaccia di rete (NIC), se la scheda di interfaccia di rete supporta la modalità promiscua. In un segmento LAN con un hub di rete, una scheda di interfaccia di rete che supporta la modalità promiscua acquisisce tutto il traffico IPv4 o IPv6 sulla LAN, incluso il traffico tra altri computer nello stesso segmento LAN. Tutti i pacchetti acquisiti (IPv4 o IPv6, a seconda del socket) verranno recapitati al socket non elaborato. Questa opzione non acquisisce altri pacchetti (ad esempio pacchetti ARP, IPX e NetBEUI) sull'interfaccia. Netmon usa la stessa modalità per l'interfaccia di rete, ma non usa questa opzione per acquisire il traffico. |
| **RC \_ SOCKETLEVELONLY** | Questa funzionalità non è attualmente implementata, quindi l'impostazione di questa opzione non ha alcun effetto. |
| **RCLEVEL \_ IPLEVEL** | Abilitare questa opzione in modo che un socket IPv4 o IPv6 riceva tutti i pacchetti a livello ip passando attraverso un'interfaccia di rete. Questa opzione non abilita la modalità promiscua nella scheda di interfaccia di rete. Questa opzione influisce solo sull'elaborazione dei pacchetti a livello di IP. La scheda di interfaccia di rete riceve comunque solo i pacchetti indirizzati agli indirizzi unicast e multicast configurati. Tuttavia, un socket con questa opzione abilitata riceverà non solo i pacchetti indirizzati a indirizzi IP specifici, ma riceverà tutti i pacchetti IPv4 o IPv6 ricevuti dalla scheda di interfaccia di rete. Questa opzione non acquisisce altri pacchetti (ad esempio ARP, IPX e NetBEUI) ricevuti sull'interfaccia. |

### <a name="cbinbuffer"></a>cbInBuffer

Dimensione, in byte, del buffer di input.
Questo parametro deve essere uguale o maggiore della dimensione del valore di **RCVALL_VALUE** a cui punta *il parametro lpvInBuffer.*

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntatore al buffer di output.
Questo parametro non è usato per questa operazione.

### <a name="cboutbuffer"></a>cbOutBuffer

Dimensione, in byte, del buffer di output.
Questo parametro non è usato per questa operazione.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Puntatore a una variabile che riceve le dimensioni, in byte, dei dati archiviati nel buffer di output.
Questo parametro non è usato per questa operazione.

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

Puntatore a una [**struttura WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) che deve essere utilizzata dal provider in una chiamata successiva a [**WPUQueueApc.**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)
Il provider deve archiviare la struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a cui si fa riferimento (non il puntatore allo stesso) fino al termine della [**funzione WPUQueueApc.**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)

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
| **OPERAZIONE WSA \_ \_ INTERROTTA** | Un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione **SIO_FLUSH** comando IOCTL. |
| **WSAEFAULT** | Il *parametro lpOverlapped* o *lpCompletionRoutine* non è completamente contenuto in una parte valida dello spazio degli indirizzi utente. |
| **WSAEINPROGRESS** | La funzione viene richiamata quando è in corso un callback. |
| **WSAEINTR** | Un'operazione di blocco è stata interrotta. |
| **WSAEINVAL** | Il *parametro dwIoControlCode* non è un comando valido o un parametro di input specificato non è accettabile oppure il comando non è applicabile al tipo di socket specificato. Questo errore viene restituito anche se il *parametro cbInBuffer* è minore di o se il parametro `sizeof(UCHAR)` *lpvInBuffer* punta a un valore che non è RCVALL_VALUE di enumerazione.  Questo errore può essere restituito anche se non è possibile trovare l'interfaccia di rete associata al socket. Ciò può verificarsi se l'interfaccia di rete associata al socket viene eliminata o rimossa (ad esempio, un dispositivo di rete PCMCIA o USB rimosso). |
| **WSAENETDOWN** | Errore del sottosistema di rete. |
| **WSAENOBUFS** | Non è disponibile spazio nel buffer. |
| **WSAENOPROTOOPT** | L'opzione socket non è supportata nel protocollo specificato. |
| **Wsaenotsock** | Il descrittore *s* non è un socket. |
| **WSAEOPNOTSUPP** | Il comando IOCTL specificato non è supportato. Questo errore viene restituito se **SIO \_ RC RPC** IOCTL non è supportato dal provider di trasporto. |

## <a name="remarks"></a>Commenti

**SIO \_ RC RPC** IOCTL è supportato in Windows 2000 e versioni successive del sistema operativo.

**L'ioCTL SIO \_ RC UDP** consente a un socket di ricevere tutti i pacchetti IPv4 o IPv6 su un'interfaccia di rete.
L'handle socket passato alla [**funzione WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** deve essere uno dei seguenti:

* Un socket IPv4 creato con la famiglia di indirizzi impostata su AF_INET, il tipo di socket impostato su SOCK_RAW e il protocollo impostato su IPPROTO_IP.
* Un socket IPv6 creato con la famiglia di indirizzi impostata su AF_INET6, il tipo di socket impostato su SOCK_RAW e il protocollo impostato su IPPROTO_IPV6.

Per altre informazioni sui socket non elaborati, vedere [**Tcp/IP Raw Sockets**](/windows/desktop/winsock/tcp-ip-raw-sockets-2).

Il socket deve anche essere associato a un'interfaccia IPv4 o IPv6 locale esplicita, il che significa che non è possibile eseguire l'associazione a **INADDR \_ ANY** o **in6addr \_ any**.

Dopo che il socket è stato associato e l'IOCTL è stato completato correttamente, le chiamate alle funzioni [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv) o [**recv restituiscono**](/windows/desktop/api/winsock/nf-winsock-recv) datagrammi IPv4 che passano attraverso l'interfaccia IPv4 specificata o restituiscono datagrammi IPv6 che passano attraverso l'interfaccia IPv6 specificata.
Si noti che è necessario fornire un buffer sufficientemente grande.
L'impostazione di questo ioCTL acquisisce solo pacchetti IPv4 o IPv6 su una determinata interfaccia.
Questo IOCTL non acquisisce altri pacchetti (ad esempio pacchetti ARP, IPX e NetBEUI) sull'interfaccia.

Un socket associato a un'interfaccia locale specifica con **SIO \_ RCVALL** IOCTL riceverà solo pacchetti che passano attraverso tale interfaccia.
Non riceverà pacchetti ricevuti su un'altra interfaccia e verrà inoltrato in un'altra interfaccia diversa dal socket associato con **SIO \_ RCVALL** IOCTL.

In Windows Server 2008 e versioni precedenti, l'impostazione **SIO \_ RCVALL** IOCTL non acquisisce i pacchetti locali inviati da un'interfaccia di rete.
Sono inclusi i pacchetti ricevuti su un'altra interfaccia e inoltrati all'interfaccia di rete specificata per **SIO \_ RCVALL** IOCTL.

In Windows 7 e Windows Server 2008 R2, questa operazione è stata modificata in modo da acquisire anche i pacchetti locali inviati da un'interfaccia di rete.
Sono inclusi i pacchetti ricevuti in un'altra interfaccia e quindi inoltrati all'interfaccia di rete associata al socket con **SIO \_ RCVALL** IOCTL.

L'impostazione di questo IOCTL richiede privilegi di amministratore nel computer locale.

Questa funzionalità viene talvolta definita modalità promiscua.
Qualsiasi modifica diretta dall'applicazione di questa opzione a un'interfaccia e quindi a un'altra interfaccia con una singola chiamata che usa questo IOCTL non è supportata.
Un'applicazione deve prima usare questo IOCTL per disattivare il comportamento nella prima interfaccia e quindi usare questo IOCTL per abilitare il comportamento in una nuova interfaccia.

## <a name="see-also"></a>Vedi anche

[**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**Socket non elaborati TCP/IP**](/windows/desktop/winsock/tcp-ip-raw-sockets-2)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**Wsaioctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
