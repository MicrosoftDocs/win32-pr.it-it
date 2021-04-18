---
description: Consente a un'applicazione di abilitare o disabilitare la restituzione di informazioni sui pacchetti mediante la funzione WSARecvMsg su un socket IPv6.
ms.assetid: 7BF17538-BE92-44FE-BA3C-6B44F61D478A
title: Opzione socket IPV6_PKTINFO (Ws2ipdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5afd5b19cbaba7f6a66f5ba6fbd85d74eb2f2e3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306940"
---
# <a name="ipv6_pktinfo-socket-option"></a>IPV6 \_ pktinfo socket-opzione

L' \_ opzione pktinfo socket IPv6 consente a un'applicazione di abilitare o disabilitare la restituzione di informazioni sui pacchetti mediante la funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) su un socket IPv6.

Per eseguire una query sullo stato di questa opzione socket, chiamare la funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) . Per impostare questa opzione, chiamare la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) con i parametri seguenti.

## <a name="socket-option-value"></a>Valore dell'opzione socket

La costante che rappresenta l'opzione del socket è 19.

## <a name="syntax"></a>Sintassi


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IPV6,   // level
  (int) IPV6_PKTINFO, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IPV6,   // level
  (int) IPV6_PKTINFO, // optname
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

Livello in corrispondenza del quale è definita l'opzione. Usare **IPPROTO \_ IPv6** per questa operazione.

</dd> <dt>

*optname* \[ in\]
</dt> <dd>

Opzione socket per la quale ottenere o impostare il valore. Usare \_ pktinfo IPv6 per questa operazione.

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

La funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) chiamata con l' \_ opzione socket pktinfo IPv6 consente a un'applicazione di determinare se le informazioni sui pacchetti devono essere restituite dalla funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)per un socket IPv6.

La funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) chiamata con l' \_ opzione socket pktinfo IPv6 consente a un'applicazione di abilitare o disabilitare la restituzione di informazioni sui pacchetti mediante la funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) . Per \_ impostazione predefinita, l'opzione pktinfo IPv6 per un socket è disabilitata (impostata su **false**).

Quando questa opzione socket è abilitata in un socket IPv6 di **tipo Sock \_ DGRAM** o **Sock \_ RAW**, la funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) restituisce informazioni sui pacchetti nella struttura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) a cui punta il parametro *lpMsg* . Uno degli oggetti dati del controllo nella struttura **WSAMSG** restituita conterrà una [**struttura \_ pktinfo IN6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) utilizzata per archiviare le informazioni relative all'indirizzo del pacchetto ricevuto.

Per i datagrammi ricevuti dalla funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) su IPv6, il membro del **controllo** della struttura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) ricevuta conterrà una struttura [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) che contiene una struttura **WSACMSGHDR** . Il membro del **\_ livello cmsg** di questa struttura **WSACMSGHDR** conterrà **IPPROTO \_ IPv6**, il membro di **\_ tipo cmsg** di questa struttura conterrà **IPv6 \_ pktinfo** e il membro **\_ dati cmsg** conterrebbe una struttura IN6 [**\_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) utilizzata per archiviare le informazioni sull'indirizzo del pacchetto IPv6 ricevute. L'indirizzo IPv6 nella struttura **\_ pktinfo di IN6** è l'indirizzo IPv6 dal quale è stato ricevuto il pacchetto.

Per un socket di datagramma a doppio stack, se un'applicazione richiede che la funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) restituisca informazioni sui pacchetti in una struttura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) per datagrammi ricevuti su IPv4, l'opzione socket [IP \_ pktinfo](ip-pktinfo.md) deve essere impostata su true nel socket. Se solo l' \_ opzione pktinfo IPv6 è impostata su true nel socket, le informazioni sui pacchetti verranno fornite per i datagrammi ricevuti su IPv6, ma potrebbero non essere fornite per datagrammi ricevuti tramite IPv4.

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

[**\_pktinfo IN6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo)
</dt> <dt>

[\_pktinfo IP](ip-pktinfo.md)
</dt> <dt>

[**\_Opzioni socket IPv6 IPPROTO**](ipproto-ipv6-socket-options.md)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**presa**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)
</dt> <dt>

[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> </dl>

 

 
