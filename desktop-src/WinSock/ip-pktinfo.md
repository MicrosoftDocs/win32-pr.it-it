---
description: Consente a un'applicazione di abilitare o disabilitare la restituzione di informazioni sui pacchetti da parte della funzione WSARecvMsg in un socket IPv4.
ms.assetid: C6246899-0220-4F88-B43B-CED1B1FF7DC3
title: IP_PKTINFO socket (Ws2ipdef.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ba653b4ece11086706493b920e1ed650b66eecdd6e788a5edfe259cf9eb9f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097791"
---
# <a name="ip_pktinfo-socket-option"></a>Opzione \_ socket IP PKTINFO

L'opzione socket IP PKTINFO consente a un'applicazione di abilitare o disabilitare la restituzione di informazioni sui pacchetti da parte della funzione \_ [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) in un socket IPv4.

Per eseguire una query sullo stato di questa opzione socket, chiamare la [**funzione getsockopt.**](/windows/desktop/api/winsock/nf-winsock-getsockopt) Per impostare questa opzione, chiamare la [**funzione setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) con i parametri seguenti.

## <a name="socket-option-value"></a>Valore dell'opzione socket

La costante che rappresenta questa opzione socket è 19.

## <a name="syntax"></a>Sintassi


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IP,   // level
  (int) IP_PKTINFO, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IP,   // level
  (int) IP_PKTINFO, // optname
  (char *) optval, // input buffer,
  (int) optlen,  // size of input buffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*s* \[ in\]
</dt> <dd>

Descrittore che identifica il socket.

</dd> <dt>

*level* \[ Pollici\]
</dt> <dd>

Livello al quale è definita l'opzione. Usare **IPPROTO \_ IP** per questa operazione.

</dd> <dt>

*optname* \[ Pollici\]
</dt> <dd>

Opzione socket per cui ottenere o impostare il valore. Usare IP \_ PKTINFO per questa operazione.

</dd> <dt>

*optval* \[ Cambio\]
</dt> <dd>

Puntatore al buffer contenente il valore per l'opzione da impostare. Questo parametro deve puntare al buffer uguale o maggiore della dimensione di un **valore DWORD.**

Questo valore viene considerato come un valore booleano con 0 usato per indicare **FALSE** (disabilitato) e un valore diverso da zero per indicare **TRUE** (abilitato).

</dd> <dt>

*optlen* \[ in, out\]
</dt> <dd>

Puntatore alla dimensione, in byte, del buffer *optval.* Questa dimensione deve essere uguale o maggiore della dimensione di un **valore DWORD.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, la [**funzione getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) o [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) restituisce zero.

Se l'operazione non riesce, viene restituito il valore SOCKET ERROR ed è possibile recuperare un codice di errore specifico chiamando \_ [**WSAGetLastError.**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)



| Codice di errore                                                                                                                                              | Significato                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Prima di usare questa funzione, è necessario che venga eseguita una chiamata [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) con esito positivo.<br/>                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | Errore del sottosistema di rete.<br/>                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Uno dei *parametri optval* o *optlen* punta alla memoria che non si trova in una parte valida dello spazio degli indirizzi utente. Questo errore viene restituito anche se il valore a cui punta il *parametro optlen* è minore della dimensione di un **valore DWORD.**<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | È in corso Windows blocco della chiamata a Sockets 1.1 oppure il provider di servizi sta ancora elaborando una funzione di callback.<br/>                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Argomento fornito non valido. Questo errore viene restituito se il *parametro level* è sconosciuto o non valido. In Windows Vista e versioni successive, questo errore viene restituito anche se il socket si trova in uno stato di transizione.<br/>                                     |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | L'opzione è sconosciuta o non è supportata dalla famiglia di protocolli indicata. Questo errore viene restituito *se* il parametro di tipo per il descrittore del socket passato nel parametro *s* non è **SOCK \_ DGRAM** o **SOCK \_ RAW.** <br/>                          |
| <dl> <dt>**[Wsaenotsock](windows-sockets-error-codes-2.md)**</dt> </dl>             | Il descrittore non è un socket.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Commenti

La [**funzione getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) chiamata con l'opzione socket IP PKTINFO consente a un'applicazione di determinare se le informazioni sui pacchetti devono essere restituite dalla funzione \_ LPFN_WSARECVMSG [**(WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)per un socket IPv4.

La [**funzione setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) chiamata con l'opzione socket IP PKTINFO consente a un'applicazione di abilitare o disabilitare la restituzione di informazioni sui pacchetti da parte della funzione \_ LPFN_WSARECVMSG [**(WSARecvMsg).**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) \_L'opzione IP PKTINFO per un socket è disabilitata (impostata su **FALSE)** per impostazione predefinita.

Quando questa opzione socket è abilitata in un socket IPv4 di tipo **SOCK \_ DGRAM** o **SOCK \_ RAW,** la funzione [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) restituisce informazioni sui pacchetti nella struttura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) a cui punta il *parametro lpMsg.* Uno degli oggetti dati di controllo nella struttura **WSAMSG** restituita conterrà una [**struttura in \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) utilizzata per archiviare le informazioni sull'indirizzo del pacchetto ricevuto.

Per i datagrammi ricevuti dalla [**funzione LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) su IPv4, il membro **Control** della struttura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) ricevuta conterrà una struttura [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) che contiene una struttura **WSACMSGHDR.** Il membro del livello cmsg di questa struttura **WSACMSGHDR** conterrà **\_ IPPROTO IP**, il membro del tipo **cmsg \_** di questa struttura conterrà IP **\_ PKTINFO** e il membro dati **cmsg \_** conterrà una struttura [**in \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) usata per archiviare le informazioni sull'indirizzo del pacchetto IPv4 ricevuto. **\_** L'indirizzo IPv4 nella **struttura in \_ pktinfo** è l'indirizzo IPv4 da cui è stato ricevuto il pacchetto.

Per un socket di datagramma dual stack, se un'applicazione richiede la funzione [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) per restituire informazioni sui pacchetti in una struttura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) per i datagrammi ricevuti tramite IPv4, l'opzione del socket IP PKTINFO deve essere impostata su \_ true nel socket. Se solo l'opzione [ \_ IPV6 PKTINFO](ipv6-pktinfo.md) è impostata su true nel socket, verranno fornite informazioni sui pacchetti per i datagrammi ricevuti tramite IPv6, ma potrebbero non essere disponibili per i datagrammi ricevuti tramite IPv4.

Se un'applicazione tenta di impostare l'opzione socket IP PKTINFO su un socket di datagramma a doppio stack e IPv4 è disabilitato nel sistema, la funzione \_ [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) avrà esito negativo e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituirà un errore [WSAEINVAL](windows-sockets-error-codes-2.md). Questo stesso errore viene restituito anche dalla **funzione setsockopt** come risultato di altri errori. Se un'applicazione tenta di impostare un'opzione socket a livello IP IPPROTO in un socket a doppio stack e ha esito negativo con \_ [WSAEINVAL,](windows-sockets-error-codes-2.md)l'applicazione deve determinare se IPv4 è disabilitato nel computer locale. Un metodo che può essere usato per rilevare se IPv4 è abilitato o disabilitato è chiamare la funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) con il *parametro af* impostato su AF INET per provare a creare un \_ socket IPv4. Se la **funzione socket** ha esito negativo e **WSAGetLastError** restituisce un errore [WSAEAFNOSUPPORT,](windows-sockets-error-codes-2.md)significa che IPv4 non è abilitato. In questo caso, un errore della funzione **setsockopt** durante il tentativo di impostare l'opzione socket IP \_ PKTINFO può essere ignorato dall'applicazione. In caso contrario, un errore durante il tentativo di impostare \_ l'opzione socket IP PKTINFO deve essere considerato un errore imprevisto.

Si noti che il file di intestazione *Ws2ipdef.h* viene incluso automaticamente in *Ws2tcpip.h* e non deve mai essere usato direttamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                                |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Ws2ipdef.h (includere Ws2tcpip.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Socket dual stack](dual-stack-sockets.md)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**in \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo)
</dt> <dt>

[**Opzioni socket \_ IPPROTO**](ipproto-ip-socket-options.md)
</dt> <dt>

[IPV6 \_ PKTINFO](ipv6-pktinfo.md)
</dt> <dt>

[**Setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)
</dt> <dt>

[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> </dl>

 

 
