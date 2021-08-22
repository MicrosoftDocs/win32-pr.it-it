---
description: La tabella seguente descrive le opzioni del socket UDP IPPROTO che si applicano ai socket creati per le famiglie di indirizzi \_ IPv4 e IPv6 (AF INET e AF INET6) con il parametro del protocollo per la funzione socket specificata come \_ UDP \_ (IPPROTO \_ UDP).
ms.assetid: 579448a1-22af-488f-a1f5-97ba69a15524
title: Opzioni socket IPPROTO_UDP
ms.topic: article
ms.date: 10/02/2019
ms.openlocfilehash: 763e45a78ffd8bfed15d09f4e77bc17be71ccc110499d8937b60b49294f499c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051479"
---
# <a name="ipproto_udp-socket-options"></a>Opzioni socket UDP IPPROTO \_

La tabella seguente descrive le opzioni del socket **\_ UDP IPPROTO** che si applicano ai socket creati per le famiglie di indirizzi IPv4 e IPv6 (AF INET e AF INET6) con il parametro del protocollo per la funzione socket specificata come \_ UDP \_ (IPPROTO  [](/windows/win32/api/Winsock2/nf-winsock2-socket) \_ UDP). Per altre informazioni su come ottenere e impostare le opzioni socket, vedere le pagine di riferimento sulle funzioni [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) e [**setsockopt.**](/windows/win32/api/winsock/nf-winsock-setsockopt)

Per enumerare i protocolli e individuare le proprietà supportate per ogni protocollo installato, usare la funzione [**WSAEnumProtocols**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/win32/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32.**](/windows/win32/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

## <a name="options"></a>Opzioni

| Opzione | Recupero | Impostazione | Tipo Optval | Descrizione |
|-|-|-|-|-|
| UDP \_ CHECKSUM \_ COVERAGE (ws2tcpip.h) | sì | sì | DWORD (booleano) | Se **TRUE,** i datagrammi UDP vengono inviati con un checksum. |
| UDP \_ NOCHECKSUM (ws2tcpip.h) | sì | sì | DWORD (booleano) | Se **TRUE,** i datagrammi UDP vengono inviati con il checksum pari a zero. Obbligatorio per i provider di servizi. Se un provider di servizi non dispone di un meccanismo per disabilitare il calcolo del checksum UDP, può semplicemente archiviare questa opzione senza eseguire alcuna azione. Questa opzione non è supportata per IPv6. |
| UDP_RECV_MAX_COALESCED_SIZE (ws2ipdef.h; include ws2tcpip.h) | sì | sì | DWORD | Se impostato su un valore diverso da zero, è possibile che più datagrammi ricevuti vengano uniti in un singolo buffer di messaggi prima di essere indicati all'applicazione. Il valore dell'opzione rappresenta la dimensione massima in byte dei messaggi uniti che possono essere indicati all'applicazione. I messaggi non uniti maggiori del valore dell'opzione possono comunque essere indicati. Il valore predefinito è 0 (nessuna coalescing). I datagrammi verranno uniti solo se hanno origine dallo stesso indirizzo di origine e dalla stessa porta. Tutti i datagrammi uniti avranno le stesse dimensioni ad eccezione &mdash; dell'ultimo datagramma, che può essere più piccolo. Se l'applicazione vuole recuperare le dimensioni del datagramma (tranne l'ultimo datagramma, che può essere diverso) che sono state coalesce, è necessario usare un'API di ricezione che supporti le informazioni di controllo (ad esempio [**LPFN_WSARECVMSG (WSARecvMsg).**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) La dimensione di tutti i messaggi,  ad UDP_COALESCED_INFO l'ultimo messaggio, è di tipo DWORD. Per l'incoerenza dei tipi, l'applicazione deve usare le funzioni [WSAGetUdpRecvMaxCoalescedSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudprecvmaxcoalescedsize) e [WSASetUdpRecvMaxCoalescedSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudprecvmaxcoalescedsize) anziché direttamente l'opzione socket. |
| UDP_SEND_MSG_SIZE (ws2ipdef.h; include ws2tcpip.h) | sì | sì | DWORD | Se impostato su un valore diverso da zero, i buffer inviati dall'applicazione vengono suddivisi in più messaggi dallo stack di rete. Il valore dell'opzione rappresenta le dimensioni di ogni messaggio suddiviso. Il valore dell'opzione è rappresentato in byte. Le dimensioni dell'ultimo segmento possono essere minori del valore dell'opzione . Il valore predefinito è 0 (nessuna segmentazione). Per evitare la frammentazione IP, l'applicazione deve impostare un valore inferiore al valore MTU del percorso delle destinazioni. Per l'a protezione dei tipi, l'applicazione deve usare direttamente le funzioni [WSAGetUdpSendMessageSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudpsendmessagesize) e [WSASetUdpSendMessageSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudpsendmessagesize) anziché l'opzione socket. |

## <a name="legacy-windows-support-for-ipproto_udp-options"></a>Supporto Windows legacy per le opzioni UDP IPPROTO \_

**UDP \_ CHECKSUM \_ COVERAGE** non è disponibile in Windows 2000 e Windows NT4. **UDP \_ CHECKSUM \_ COVERAGE e** UDP **\_ NOCHECKSUM** non sono disponibili Windows 9x/Me. 

## <a name="remarks"></a>Commenti

In Microsoft Windows Software Development Kit (SDK) rilasciato per Windows Vista e versioni successive, l'organizzazione dei file di intestazione è stata modificata e il livello **\_ UDP IPPROTO** è definito nel file di intestazione *Ws2def.h* che viene automaticamente incluso nel file di intestazione *Winsock2.h.* Le opzioni del socket **\_ UDP IPPROTO** sono definite nel file di intestazione *Ws2tcpip.h.* Il file *di intestazione Ws2def.h* non deve mai essere usato direttamente.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione<br/> | <dl> <dt>ws2ipdef.h (include ws2tcpip.h) e ws2tcpip.h</dt> <dt>Winsock2.h in Windows Server 2003, Windows XP e Windows 2000</dt> </dl> |
