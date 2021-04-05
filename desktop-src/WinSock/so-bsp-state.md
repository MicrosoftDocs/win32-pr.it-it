---
description: Restituisce l'indirizzo locale, la porta locale, l'indirizzo remoto, la porta remota, il tipo di socket e il protocollo utilizzati da un socket.
ms.assetid: 2628f47e-3e73-4e02-91b8-ba4cb0800864
title: Opzione socket SO_BSP_STATE (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d10e391d70dd67190e1aec803036d019261c9000
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755058"
---
# <a name="so_bsp_state-socket-option"></a>\_ \_ Opzione socket stato BSP

L'opzione **so \_ BSP \_ state** socket restituisce l'indirizzo locale, la porta locale, l'indirizzo remoto, la porta remota, il tipo di socket e il protocollo usati da un socket.

Per eseguire questa operazione, chiamare la funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) con i parametri seguenti.

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

*livello* \[ di in\]
</dt> <dd>

Livello in corrispondenza del quale è definita l'opzione. Usare **il \_ socket Sol** per questa operazione.

</dd> <dt>

*optname* \[ in\]
</dt> <dd>

Opzione socket per la quale deve essere recuperato il valore. Usare **così \_ \_ lo stato BSP** per questa operazione.

</dd> <dt>

*optVal* \[ out\]
</dt> <dd>

Puntatore al buffer in cui deve essere restituito il valore per l'opzione richiesta. Questo parametro deve puntare a un buffer uguale o maggiore della dimensione di una struttura [**di \_ informazioni CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .

</dd> <dt>

*optlen* \[ in uscita\]
</dt> <dd>

Puntatore alla dimensione, in byte, del buffer *optVal* . Questa dimensione deve essere maggiore o uguale alla dimensione di una struttura di [**\_ informazioni CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) restituisce zero.

Se l'operazione ha esito negativo, viene restituito un valore di \_ errore socket e un codice di errore specifico può essere recuperato chiamando [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).



| Codice di errore                                                                                                                                              | Significato                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Prima di utilizzare questa funzione, è necessario che venga eseguita una chiamata [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) .<br/>                                                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | Il sottosistema di rete non è riuscito.<br/>                                                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Uno dei parametri *optVal* o *optlen* punta alla memoria che non si trova in una parte valida dello spazio degli indirizzi utente. Questo errore viene restituito anche se il valore a cui punta il parametro *optlen* è minore della dimensione di una struttura [**di \_ informazioni di CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | È in corso una chiamata di blocco di Windows Sockets 1,1 o il provider di servizi sta ancora elaborando una funzione di callback.<br/>                                                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Il parametro *Level* è sconosciuto o non valido.<br/>                                                                                                                                                                                                                                    |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | L'opzione è sconosciuta o non supportata dalla famiglia di protocolli indicata.<br/>                                                                                                                                                                                                          |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | Il descrittore non è un socket.<br/>                                                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Commenti

La funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) chiamata con l'opzione di socket **\_ \_ dello stato BSP** , recupera l'indirizzo locale, la porta locale, l'indirizzo remoto, la porta remota, il tipo di socket e il protocollo usati da un socket. L'opzione per il socket di **\_ \_ stato BSP** è compatibile con i socket IPv6 o IPv4 (le famiglie di indirizzi **AF \_ INET6** e **AF \_ inet** ).

Se la funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) ha esito positivo, le informazioni vengono restituite in una struttura di [**\_ informazioni CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) nel buffer a cui punta il parametro *optVal* . Il numero intero a cui punta *optlen* deve contenere originariamente la dimensione del buffer. al ritorno, verrà impostato sulla lunghezza, in byte, del valore restituito nel parametro *optVal* .

I membri **iSocketType** e **iProtocol** nella struttura di [**\_ informazioni CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) restituita vengono compilati per il descrittore di socket nel parametro *s* .

Se il socket è in uno stato connesso o associato, il membro **LocalAddr** della struttura di [**\_ informazioni CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) restituita verrà impostato su una struttura [sockaddr](sockaddr-2.md) che rappresenta l'indirizzo e la porta locali. Se il socket è in uno stato connesso, il membro **IndirizzoRemoto** della struttura di **\_ informazioni CSADDR** restituita verrà impostato su una struttura SOCKADDR che rappresenta l'indirizzo remoto e la porta.

Se il socket non si trova in uno stato connesso o associato, il membro **LocalAddr** della struttura di [**\_ informazioni CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) restituita viene restituito con un puntatore **null** nel membro **lpSockaddr** e il membro **iSockaddrLength** è impostato su zero. Se il socket non è in uno stato associato, il membro **IndirizzoRemoto** della struttura di **\_ informazioni CSADDR** restituita viene restituito con un **puntatore null** nel membro **lpSockaddr** e il membro **iSockaddrLength** impostato su zero.

Se la funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) ha esito negativo, i parametri *optVal* e *optlen* vengono lasciati invariati e il parametro *optVal* non punta a una struttura di [**\_ informazioni CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) restituita.

Si noti che il file di intestazione *Ws2def. h* viene incluso automaticamente in *Winsock2. h* e non deve mai essere utilizzato direttamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Ws2def. h (include Winsock2. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**\_informazioni CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)
</dt> <dt>

[SOCKADDR](sockaddr-2.md)
</dt> </dl>

 

 
