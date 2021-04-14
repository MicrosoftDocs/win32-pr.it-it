---
description: Consente a un'applicazione di abilitare o disabilitare la restituzione di informazioni sui pacchetti mediante la funzione WSARecvMsg su un socket IPv4.
ms.assetid: C6246899-0220-4F88-B43B-CED1B1FF7DC3
title: Opzione socket IP_PKTINFO (Ws2ipdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2134b31ead9efeb032b4ed72fcaedcd4cc9f67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343491"
---
# <a name="ip_pktinfo-socket-option"></a>\_Opzione socket IP pktinfo

L' \_ opzione del socket IP pktinfo consente a un'applicazione di abilitare o disabilitare la restituzione di informazioni sui pacchetti tramite la funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) su un socket IPv4.

Per eseguire una query sullo stato di questa opzione socket, chiamare la funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) . Per impostare questa opzione, chiamare la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) con i parametri seguenti.

## <a name="socket-option-value"></a>Valore dell'opzione socket

La costante che rappresenta l'opzione del socket è 19.

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

*livello* \[ di in\]
</dt> <dd>

Livello in corrispondenza del quale è definita l'opzione. Usare **l' \_ IP IPPROTO** per questa operazione.

</dd> <dt>

*optname* \[ in\]
</dt> <dd>

Opzione socket per la quale ottenere o impostare il valore. Usare \_ pktinfo IP per questa operazione.

</dd> <dt>

*optVal* \[ out\]
</dt> <dd>

Puntatore al buffer che contiene il valore per l'opzione da impostare. Questo parametro deve puntare a un buffer uguale o maggiore della dimensione di un valore **DWORD** .

Questo valore viene considerato come un valore booleano con 0 usato per indicare **false** (disabilitato) e un valore diverso da zero per indicare **true** (abilitato).

</dd> <dt>

*optlen* \[ in uscita\]
</dt> <dd>

Puntatore alla dimensione, in byte, del buffer *optVal* . Questa dimensione deve essere maggiore o uguale alla dimensione di un valore **DWORD** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, la funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) o [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) restituisce zero.

Se l'operazione ha esito negativo, viene restituito un valore di \_ errore socket e un codice di errore specifico può essere recuperato chiamando [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).



| Codice di errore                                                                                                                                              | Significato                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Prima di utilizzare questa funzione, è necessario che venga eseguita una chiamata [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) .<br/>                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | Il sottosistema di rete non è riuscito.<br/>                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Uno dei parametri *optVal* o *optlen* punta alla memoria che non si trova in una parte valida dello spazio degli indirizzi utente. Questo errore viene restituito anche se il valore a cui punta il parametro *optlen* è minore della dimensione di un valore **DWORD** .<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | È in corso una chiamata di blocco di Windows Sockets 1,1 o il provider di servizi sta ancora elaborando una funzione di callback.<br/>                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Argomento fornito non valido. Questo errore viene restituito se il parametro *Level* è sconosciuto o non valido. In Windows Vista e versioni successive questo errore viene restituito anche se il socket si trovava in uno stato di transizione.<br/>                                     |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | L'opzione è sconosciuta o non supportata dalla famiglia di protocolli indicata. Questo errore viene restituito se il parametro di *tipo* per il descrittore di socket passato al parametro *s* non è **Sock \_ DGRAM** o **Sock \_ RAW**. <br/>                          |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | Il descrittore non è un socket.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Commenti

La funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) chiamata con l' \_ opzione pktinfo socket IP consente a un'applicazione di determinare se le informazioni sui pacchetti devono essere restituite dalla funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)per un socket IPv4.

La funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) chiamata con l' \_ opzione pktinfo socket IP consente a un'applicazione di abilitare o disabilitare la restituzione di informazioni sui pacchetti mediante la funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) . Per \_ impostazione predefinita, l'opzione pktinfo IP per un socket è disabilitata (impostata su **false**).

Quando questa opzione socket è abilitata in un socket IPv4 di **tipo Sock \_ DGRAM** o **Sock \_ RAW**, la funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) restituisce informazioni sui pacchetti nella struttura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) a cui punta il parametro *lpMsg* . Uno degli oggetti dati del controllo nella struttura **WSAMSG** restituita conterrà un oggetto [**nella struttura \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) utilizzata per archiviare le informazioni relative all'indirizzo del pacchetto ricevuto.

Per i datagrammi ricevuti dalla funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) su IPv4, il membro del **controllo** della struttura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) ricevuta conterrà una struttura [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) che contiene una struttura **WSACMSGHDR** . Il membro del **\_ livello cmsg** di questa struttura **WSACMSGHDR** conterrà l'indirizzo **\_ IP IPPROTO**, il membro di **\_ tipo cmsg** di questa struttura conterrà **IP \_ pktinfo** e il membro **\_ dati cmsg** conterrà un oggetto [**nella struttura \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) utilizzato per archiviare le informazioni sull'indirizzo del pacchetto IPv4 ricevute. L'indirizzo IPv4 nella struttura **\_ pktinfo** è l'indirizzo IPv4 dal quale è stato ricevuto il pacchetto.

Per un socket di datagramma a doppio stack, se un'applicazione richiede che la funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) restituisca informazioni sui pacchetti in una struttura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) per datagrammi ricevuti su IPv4, l' \_ opzione socket IP pktinfo deve essere impostata su true nel socket. Se solo l' [opzione \_ pktinfo IPv6](ipv6-pktinfo.md) è impostata su true nel socket, le informazioni sui pacchetti verranno fornite per i datagrammi ricevuti su IPv6, ma potrebbero non essere fornite per datagrammi ricevuti tramite IPv4.

Se un'applicazione prova a impostare l' \_ opzione del socket pktinfo IP su un socket di datagramma a doppio stack e IPv4 è disabilitato nel sistema, la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) avrà esito negativo e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituirà un errore di [WSAEINVAL](windows-sockets-error-codes-2.md). Questo stesso errore viene inoltre restituito dalla funzione **setsockopt** come risultato di altri errori. Se un'applicazione tenta di impostare un' \_ opzione socket a livello IP IPPROTO in un socket a doppio stack e non riesce con [WSAEINVAL](windows-sockets-error-codes-2.md), l'applicazione deve determinare se IPv4 è disabilitato nel computer locale. Un metodo che può essere usato per rilevare se IPv4 è abilitato o disabilitato consiste nel chiamare la funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) con il parametro *AF* impostato su AF \_ inet per provare a creare un socket IPv4. Se la funzione **socket** ha esito negativo e **WSAGetLastError** restituisce un errore di [WSAEAFNOSUPPORT](windows-sockets-error-codes-2.md), significa che IPv4 non è abilitato. In questo caso, un errore di funzione **setsockopt** durante il tentativo di impostare l' \_ opzione del socket IP pktinfo può essere ignorato dall'applicazione. In caso contrario, un errore durante il tentativo di impostare l' \_ opzione del socket pktinfo IP deve essere considerato un errore imprevisto.

Si noti che il file di intestazione *Ws2ipdef. h* viene incluso automaticamente in *Ws2tcpip. h* e non deve mai essere utilizzato direttamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                                |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Ws2ipdef. h (include Ws2tcpip. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Socket dual stack](dual-stack-sockets.md)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**in \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo)
</dt> <dt>

[**\_Opzioni del socket IP IPPROTO**](ipproto-ip-socket-options.md)
</dt> <dt>

[\_Pktinfo IPv6](ipv6-pktinfo.md)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**presa**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)
</dt> <dt>

[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> </dl>

 

 
