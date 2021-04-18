---
description: La tabella seguente descrive le \_ Opzioni del socket UDP IPPROTO che si applicano ai socket creati per le famiglie di indirizzi IPv4 e IPv6 (AF \_ inet e AF \_ INET6) con il parametro Protocol per la funzione Socket specificata come UDP (UDP IPPROTO \_ ).
ms.assetid: 579448a1-22af-488f-a1f5-97ba69a15524
title: Opzioni socket IPPROTO_UDP
ms.topic: article
ms.date: 10/02/2019
ms.openlocfilehash: 6f1f25ebae34d7db4290ab23bbf799fc0e0b68df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327130"
---
# <a name="ipproto_udp-socket-options"></a>\_Opzioni socket UDP IPPROTO

La tabella seguente descrive le opzioni del socket **\_ UDP IPPROTO** che si applicano ai socket creati per le famiglie di indirizzi IPv4 e IPv6 (AF \_ inet e AF \_ INET6) con il parametro *Protocol* per la funzione [**socket**](/windows/win32/api/Winsock2/nf-winsock2-socket) specificata come UDP (UDP IPPROTO \_ ). Vedere le pagine di riferimento per le funzioni [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) e [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) per altre informazioni su come ottenere e impostare le opzioni del socket.

Per enumerare i protocolli e individuare le proprietà supportate per ogni protocollo installato, usare la funzione [**WSAEnumProtocols**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/win32/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32**](/windows/win32/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

## <a name="options"></a>Opzioni

| Opzione | Recupero | Set | Tipo optVal | Descrizione |
|-|-|-|-|-|
| \_Copertura checksum UDP \_ (Ws2tcpip. h) | sì | sì | DWORD (booleano) | Se **true**, i datagrammi UDP vengono inviati con un checksum. |
| UDP \_ NoChecksum (Ws2tcpip. h) | sì | sì | DWORD (booleano) | Se è **true**, i datagrammi UDP vengono inviati con il checksum di zero. Obbligatorio per i provider di servizi. Se un provider di servizi non dispone di un meccanismo per disabilitare il calcolo del checksum UDP, può semplicemente archiviare questa opzione senza eseguire alcuna azione. Questa opzione non è supportata per IPv6. |
| UDP_RECV_MAX_COALESCED_SIZE (ws2ipdef. h; Includi Ws2tcpip. h) | sì | sì | DWORD | Quando è impostato su un valore diverso da zero, è possibile che più datagrammi ricevuti vengano uniti in un singolo buffer di messaggi prima di essere indicati per l'applicazione. Il valore dell'opzione rappresenta la dimensione massima in byte dei messaggi che possono essere indicati all'applicazione. I messaggi non Uniti di dimensioni maggiori del valore dell'opzione possono comunque essere indicati. Il valore predefinito è 0 (nessuna Unione). I datagrammi verranno uniti solo se originati dallo stesso indirizzo di origine e dalla stessa porta. Tutti i datagrammi Uniti saranno della stessa dimensione &mdash; , ad eccezione dell'ultimo datagramma, che può essere minore. Se l'applicazione desidera recuperare le dimensioni del datagramma (ad eccezione dell'ultimo datagramma, che può variare), è necessario utilizzare un'API di ricezione che supporti le informazioni di controllo (ad esempio [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)). La dimensione di tutto tranne l'ultimo messaggio è reperibile nel messaggio di controllo **UDP_COALESCED_INFO** , che è di tipo DWORD. Per l'indipendenza dai tipi, l'applicazione deve usare le funzioni [WSAGetUdpRecvMaxCoalescedSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudprecvmaxcoalescedsize) e [WSASetUdpRecvMaxCoalescedSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudprecvmaxcoalescedsize) anziché l'opzione socket direttamente. |
| UDP_SEND_MSG_SIZE (ws2ipdef. h; Includi Ws2tcpip. h) | sì | sì | DWORD | Quando è impostato su un valore diverso da zero, i buffer inviati dall'applicazione vengono suddivisi in più messaggi dallo stack di rete. Il valore dell'opzione rappresenta le dimensioni di ogni messaggio suddiviso. Il valore dell'opzione è rappresentato in byte. Le dimensioni dell'ultimo segmento possono essere minori del valore dell'opzione. Il valore predefinito è 0 (Nessuna segmentazione). L'applicazione deve impostare un valore inferiore rispetto alla MTU del percorso delle destinazioni per evitare la frammentazione IP. Per l'indipendenza dai tipi, l'applicazione deve usare le funzioni [WSAGetUdpSendMessageSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudpsendmessagesize) e [WSASetUdpSendMessageSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudpsendmessagesize) anziché l'opzione socket direttamente. |

## <a name="legacy-windows-support-for-ipproto_udp-options"></a>Supporto di Windows legacy per le \_ Opzioni UDP di IPPROTO

**UDP \_ Il \_ code coverage** non è disponibile in Windows 2000 e Windows NT4. **UDP \_ Il \_ code coverage e UDP NOchecksum** non sono disponibili in Windows 9x/Me. **\_** 

## <a name="remarks"></a>Commenti

In Microsoft Windows Software Development Kit (SDK) rilasciato per Windows Vista e versioni successive, l'organizzazione dei file di intestazione è stata modificata e il livello **\_ UDP IPPROTO** è definito nel file di intestazione *Ws2def. h* , che viene automaticamente incluso nel file di intestazione *Winsock2. h* . Le opzioni del socket **\_ UDP IPPROTO** sono definite nel file di intestazione *Ws2tcpip. h* . Il file di intestazione *Ws2def. h* non deve mai essere utilizzato direttamente.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione<br/> | <dl> <dt>ws2ipdef. h (include Ws2tcpip. h) e Ws2tcpip. h</dt> <dt>Winsock2. h in Windows Server 2003, Windows XP e Windows 2000</dt> </dl> |
