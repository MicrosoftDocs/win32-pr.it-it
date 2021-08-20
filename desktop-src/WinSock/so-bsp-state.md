---
description: Restituisce l'indirizzo locale, la porta locale, l'indirizzo remoto, la porta remota, il tipo di socket e il protocollo utilizzati da un socket.
ms.assetid: 2628f47e-3e73-4e02-91b8-ba4cb0800864
title: SO_BSP_STATE socket (Ws2def.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ff165eaef1f773f41c93f1c9905588b8d715f64e89ea0cbf06d53eb656bc91a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118111251"
---
# <a name="so_bsp_state-socket-option"></a>Opzione \_ socket SO BSP \_ STATE

L'opzione socket **SO \_ BSP \_ STATE** restituisce l'indirizzo locale, la porta locale, l'indirizzo remoto, la porta remota, il tipo di socket e il protocollo usati da un socket.

Per eseguire questa operazione, chiamare la [**funzione getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) con i parametri seguenti.

## <a name="socket-option-value"></a>Valore dell'opzione socket

La costante che rappresenta questa opzione socket è 0x1009.

## <a name="syntax"></a>Sintassi


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_BSP_STATE, // optname
  (char *) optval,         // output buffer,
  (int) *optlen,       // size of output buffer
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

Livello al quale è definita l'opzione. Usare **SOL \_ SOCKET** per questa operazione.

</dd> <dt>

*optname* \[ Pollici\]
</dt> <dd>

Opzione socket per cui recuperare il valore. Usare **SO \_ BSP \_ STATE** per questa operazione.

</dd> <dt>

*optval* \[ Cambio\]
</dt> <dd>

Puntatore al buffer in cui deve essere restituito il valore dell'opzione richiesta. Questo parametro deve puntare al buffer uguale o maggiore delle dimensioni di una [**struttura CSADDR \_ INFO.**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)

</dd> <dt>

*optlen* \[ in, out\]
</dt> <dd>

Puntatore alla dimensione, in byte, del buffer *optval.* Queste dimensioni devono essere uguali o maggiori delle dimensioni di una [**struttura CSADDR \_ INFO.**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) restituisce zero.

Se l'operazione ha esito negativo, viene restituito il valore SOCKET ERROR e un codice di errore specifico può essere recuperato chiamando \_ [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).



| Codice di errore                                                                                                                                              | Significato                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Prima di usare questa funzione, è necessario che venga eseguita una chiamata [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) riuscita.<br/>                                                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | Il sottosistema di rete non è riuscito.<br/>                                                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Uno dei parametri *optval* o *optlen* punta alla memoria che non si trova in una parte valida dello spazio indirizzi utente. Questo errore viene restituito anche se il valore a cui punta il *parametro optlen* è minore delle dimensioni di una [**struttura CSADDR \_ INFO.**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | È in corso Windows chiamata a Sockets 1.1 o il provider di servizi sta ancora elaborando una funzione di callback.<br/>                                                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Il *parametro level* è sconosciuto o non valido.<br/>                                                                                                                                                                                                                                    |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | L'opzione è sconosciuta o non supportata dalla famiglia di protocolli indicata.<br/>                                                                                                                                                                                                          |
| <dl> <dt>**[Wsaenotsock](windows-sockets-error-codes-2.md)**</dt> </dl>             | Il descrittore non è un socket.<br/>                                                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Commenti

La [**funzione getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) chiamata con l'opzione socket **SO \_ BSP \_ STATE** recupera l'indirizzo locale, la porta locale, l'indirizzo remoto, la porta remota, il tipo di socket e il protocollo usati da un socket. L'opzione socket **SO \_ BSP \_ STATE** funziona con i socket IPv6 o IPv4 (le famiglie di indirizzi **AF \_ INET6** e **AF \_ INET).**

Se la [**funzione getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) ha esito positivo, le informazioni vengono restituite in una struttura [**CSADDR \_ INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) nel buffer a cui punta il *parametro optval.* L'intero a cui *punta optlen* deve in origine contenere le dimensioni di questo buffer. in caso di restituzione, verrà impostato sulla lunghezza, in byte, del valore restituito nel *parametro optval.*

I **membri iSocketType** e **iProtocol** nella struttura [**CSADDR \_ INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) restituita vengono compilati per il descrittore del socket nel *parametro s.*

Se il socket si trova in uno stato connesso o associato, il membro **LocalAddr** della struttura [**CSADDR \_ INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) restituita verrà impostato su una struttura [SOCKADDR](sockaddr-2.md) che rappresenta l'indirizzo locale e la porta. Se il socket è in uno stato connesso, il membro **RemoteAddr** della struttura **CSADDR \_ INFO** restituita verrà impostato su una struttura SOCKADDR che rappresenta l'indirizzo remoto e la porta.

Se il socket non si trova in uno stato connesso o associato, il membro **LocalAddr** della struttura [**CSADDR \_ INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) restituita viene restituito con un puntatore **NULL** nel membro **lpSockaddr** e il membro **iSockaddrLength** impostato su zero. Se il socket non è in uno stato associato, il membro **RemoteAddr** della struttura **CSADDR \_ INFO** restituita viene restituito con un **puntatore NULL** nel membro **lpSockaddr** e il membro **iSockaddrLength** impostato su zero.

Se la [**funzione getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) ha esito negativo, i parametri *optval* e *optlen* rimangono invariati e il *parametro optval* non punta a una struttura [**CSADDR \_ INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) restituita.

Si noti che il file di intestazione *Ws2def.h* viene incluso automaticamente in *Winsock2.h* e non deve mai essere usato direttamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Ws2def.h (includere Winsock2.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**CSADDR \_ INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)
</dt> <dt>

[SOCKADDR](sockaddr-2.md)
</dt> </dl>

 

 
