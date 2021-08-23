---
description: Consente a un'applicazione di abilitare o disabilitare la restituzione di informazioni sui pacchetti tramite la funzione WSARecvMsg in un socket IPv6.
ms.assetid: 7BF17538-BE92-44FE-BA3C-6B44F61D478A
title: IPV6_PKTINFO socket (Ws2ipdef.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1bee015e7a73b803d78ae914e71a863dec83e4f40fc1aea9f631a54b37c586a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733771"
---
# <a name="ipv6_pktinfo-socket-option"></a>Opzione \_ socket IPV6 PKTINFO

L'opzione socket IPV6 PKTINFO consente a un'applicazione di abilitare o disabilitare la restituzione di informazioni sui pacchetti tramite la funzione \_ [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) in un socket IPv6.

Per eseguire una query sullo stato di questa opzione socket, chiamare la [**funzione getsockopt.**](/windows/desktop/api/winsock/nf-winsock-getsockopt) Per impostare questa opzione, chiamare la [**funzione setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) con i parametri seguenti.

## <a name="socket-option-value"></a>Valore dell'opzione socket

La costante che rappresenta questa opzione socket è 19.

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

*level* \[ Pollici\]
</dt> <dd>

Livello al quale è definita l'opzione. Usare **IPPROTO \_ IPV6** per questa operazione.

</dd> <dt>

*optname* \[ Pollici\]
</dt> <dd>

Opzione socket per cui ottenere o impostare il valore. Usare PKTINFO IPV6 \_ per questa operazione.

</dd> <dt>

*optval* \[ Cambio\]
</dt> <dd>

Puntatore al buffer contenente il valore dell'opzione da impostare. Questo parametro deve puntare al buffer uguale o maggiore delle dimensioni di un **valore DWORD.**

Questo valore viene considerato come valore booleano con 0 usato per indicare **FALSE** (disabilitato) e un valore diverso da zero per indicare **TRUE** (abilitato).

</dd> <dt>

*optlen* \[ in, out\]
</dt> <dd>

Puntatore alla dimensione, in byte, del buffer *optval.* Questa dimensione deve essere uguale o maggiore della dimensione di un **valore DWORD.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, la [**funzione getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) o [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) restituisce zero.

Se l'operazione ha esito negativo, viene restituito il valore SOCKET ERROR e un codice di errore specifico può essere recuperato chiamando \_ [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).



| Codice di errore                                                                                                                                              | Significato                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Prima di usare questa funzione, è necessario che venga eseguita una chiamata [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) riuscita.<br/>                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | Il sottosistema di rete non è riuscito.<br/>                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Uno dei parametri *optval* o *optlen* punta alla memoria che non si trova in una parte valida dello spazio indirizzi utente. Questo errore viene restituito anche se il valore a cui punta il *parametro optlen* è minore delle dimensioni di un **valore DWORD.**<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | È in corso Windows chiamata a Sockets 1.1 o il provider di servizi sta ancora elaborando una funzione di callback.<br/>                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Argomento fornito non valido. Questo errore viene restituito se il *parametro level* è sconosciuto o non valido. In Windows Vista e versioni successive, questo errore viene restituito anche se il socket si trova in uno stato di transizione.<br/>                                     |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | L'opzione è sconosciuta o non supportata dalla famiglia di protocolli indicata. Questo errore viene restituito se il parametro *di* tipo per il descrittore socket passato nel parametro *s* non è **SOCK \_ DGRAM** o **SOCK \_ RAW.** <br/>                          |
| <dl> <dt>**[Wsaenotsock](windows-sockets-error-codes-2.md)**</dt> </dl>             | Il descrittore non è un socket.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Commenti

La [**funzione getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) chiamata con l'opzione socket IPV6 PKTINFO consente a un'applicazione di determinare se le informazioni sui pacchetti devono essere restituite dalla funzione \_ LPFN_WSARECVMSG [**(WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)per un socket IPv6.

La [**funzione setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) chiamata con l'opzione socket IPV6 PKTINFO consente a un'applicazione di abilitare o disabilitare la restituzione di informazioni sui pacchetti da parte della funzione \_ LPFN_WSARECVMSG [**(WSARecvMsg).**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) L'opzione PKTINFO IPV6 per un socket è disabilitata \_ (impostata su **FALSE)** per impostazione predefinita.

Quando questa opzione socket è abilitata in un socket IPv6 di tipo **SOCK \_ DGRAM** o **SOCK \_ RAW,** la funzione [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) restituisce informazioni sui pacchetti nella struttura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) a cui punta il *parametro lpMsg.* Uno degli oggetti dati di controllo nella struttura **WSAMSG** restituita conterrà una struttura [**in6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) usata per archiviare le informazioni sull'indirizzo del pacchetto ricevuto.

Per i datagrammi ricevuti dalla funzione [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) su IPv6, il membro **Control** della struttura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) ricevuta conterrà una struttura [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) che contiene una **struttura WSACMSGHDR.** Il membro di livello cmsg di questa struttura **WSACMSGHDR** conterrà **IPPROTO \_ IPV6,** il membro del tipo **\_ cmsg** di questa struttura conterrà **\_ PKTINFO IPV6** e il membro dati **cmsg \_** conterrà una struttura [**in6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) usata per archiviare le informazioni sull'indirizzo del pacchetto IPv6 ricevuto. **\_** L'indirizzo IPv6 nella **struttura in6 \_ pktinfo** è l'indirizzo IPv6 da cui è stato ricevuto il pacchetto.

Per un socket di datagramma a doppio stack, se un'applicazione richiede la funzione [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) per restituire informazioni sui pacchetti in una struttura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) per i datagrammi ricevuti tramite IPv4, l'opzione socket [IP \_ PKTINFO](ip-pktinfo.md) deve essere impostata su true nel socket. Se solo l'opzione PKTINFO IPV6 è impostata su true nel socket, le informazioni sui pacchetti verranno fornite per i datagrammi ricevuti tramite IPv6, ma potrebbero non essere fornite per i datagrammi ricevuti tramite \_ IPv4.

Si noti che il file di intestazione *Ws2ipdef.h* viene incluso automaticamente in *Ws2tcpip.h* e non deve mai essere usato direttamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                                |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Ws2ipdef.h (includere Ws2tcpip.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Socket a doppio stack](dual-stack-sockets.md)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**in6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo)
</dt> <dt>

[IP \_ PKTINFO](ip-pktinfo.md)
</dt> <dt>

[**Opzioni socket IPV6 IPPROTO \_**](ipproto-ipv6-socket-options.md)
</dt> <dt>

[**Setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)
</dt> <dt>

[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> </dl>

 

 
