---
description: La tabella seguente descrive le \_ Opzioni del socket TCP IPPROTO che si applicano ai socket creati per le famiglie di indirizzi IPv4 e IPv6 (AF \_ inet e AF \_ INET6) con il parametro Protocol per la funzione Socket specificata come TCP (IPPROTO \_ TCP).
ms.assetid: 2a10498d-0a0b-4a2d-941e-9aa45a1a4428
title: Opzioni socket IPPROTO_TCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20d261a639c10faa8c8ef52ba1ae88a0fbc52a16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327132"
---
# <a name="ipproto_tcp-socket-options"></a>\_Opzioni socket TCP IPPROTO

La tabella seguente descrive le opzioni del socket **\_ TCP IPPROTO** che si applicano ai socket creati per le famiglie di indirizzi IPv4 e IPv6 (AF \_ inet e AF \_ INET6) con il parametro *Protocol* per la funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) specificata come TCP (IPPROTO \_ TCP). Vedere le pagine di riferimento per le funzioni [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) per altre informazioni su come ottenere e impostare le opzioni del socket.

Per enumerare i protocolli e individuare le proprietà supportate per ogni protocollo installato, usare la funzione [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

## <a name="options"></a>Opzioni

<table>
<colgroup>
<col/>
<col/>
<col/>
<col/>
<col/>
</colgroup>
<thead>
<tr class="header">
<th>Opzione</th>
<th>Recupero</th>
<th>Set</th>
<th>Tipo optVal</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr>
<td>TCP_BSDURGENT</td>
<td>sì</td>
<td>sì</td>
<td>DWORD (booleano)</td>
<td>Se <strong>true</strong>, il provider di servizi implementa lo stile BSD (Berkeley Software Distribution) (impostazione predefinita) per la gestione dei dati accelerati. Questa opzione è l'inverso dell'opzione TCP_EXPEDITED_1122. Questa opzione può essere impostata sulla connessione una sola volta. Quando questa opzione è impostata su on, questa opzione non può essere disattivata. Questa opzione non deve essere implementata dai provider di servizi. Per impostazione predefinita, l'opzione è abilitata (impostata su <strong>true</strong>).</td>
</tr>
<tr>
<td>TCP_EXPEDITED_1122</td>
<td>sì</td>
<td>sì</td>
<td>DWORD (booleano)</td>
<td>Se <strong>true</strong>, il provider di servizi implementa i dati accelerati come specificato in RFC-1222. In caso contrario, viene utilizzato lo stile BSD (Berkeley Software Distribution) (impostazione predefinita). Questa opzione può essere impostata sulla connessione una sola volta. Quando questa opzione è impostata su on, questa opzione non può essere disattivata. Questa opzione non deve essere implementata dai provider di servizi.</td>
</tr>
<tr>
<td>TCP_FAIL_CONNECT_ON_ICMP_ERROR</td>
<td>sì</td>
<td>sì</td>
<td>DWORD (booleano)</td>
<td>Se <strong>true</strong>, una chiamata all'API Connect restituirà al ricevimento di un errore ICMP con valore WSAEHOSTUNREACH. L'indirizzo di origine dell'errore sarà quindi disponibile tramite l'opzione socket TCP_ICMP_ERROR_INFO. Se <strong>false</strong>, il socket si comporta normalmente. Il valore predefinito è Disabled (impostato su <strong>false</strong>). Per indipendenza dai tipi, è consigliabile utilizzare le funzioni <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetfailconnectonicmperror">WSAGetFailConnectOnIcmpError</a> e <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetfailconnectonicmperror">WSASetFailConnectOnIcmpError</a> anziché utilizzare direttamente l'opzione socket.</td>
</tr>
<tr>
<td>TCP_ICMP_ERROR_INFO</td>
<td>sì</td>
<td>no</td>
<td><a href="/windows/win32/api/ws2ipdef/ns-ws2ipdef-icmp_error_info">ICMP_ERROR_INFO</a></td>
<td>Recupera le informazioni di un errore ICMP ricevuto dal socket TCP durante una chiamata di connessione non riuscita. Valido solo in un socket TCP in cui TCP_FAIL_CONNECT_ON_ICMP_ERROR è stato precedentemente abilitato e <strong>Connect</strong> ha restituito WSAEHOSTUNREACH. La query non è bloccata. Se la query viene eseguita correttamente e il valore di optlen restituito è 0, non è stato ricevuto alcun errore ICMP dall'ultima chiamata di connessione. Se è stato ricevuto un errore ICMP, le informazioni saranno disponibili fino a quando non viene richiamata la <strong>connessione</strong> . Le informazioni vengono restituite come struttura <a href="/windows/win32/api/ws2ipdef/ns-ws2ipdef-icmp_error_info">ICMP_ERROR_INFO</a> . Per indipendenza dai tipi, è consigliabile usare la funzione <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsageticmperrorinfo">WSAGetIcmpErrorInfo</a> invece di usare direttamente l'opzione socket.</td>
</tr>
<tr>
<td>TCP_KEEPCNT</td>
<td>sì</td>
<td>sì</td>
<td>DWORD</td>
<td>Ottiene o imposta il numero di probe keep-alive TCP che verranno inviati prima che la connessione venga terminata. Non è consentito impostare TCP_KEEPCNT su un valore maggiore di 255.</td>
</tr>
<tr>
<td>TCP_MAXRT</td>
<td>sì</td>
<td>sì</td>
<td>DWORD</td>
<td>Se questo valore è non negativo, rappresenta il timeout di connessione desiderato in secondi. Se è-1, rappresenta una richiesta di disabilitazione del timeout di connessione (ad esempio, la connessione verrà ritrasmessa per sempre). Se il timeout di connessione è disabilitato, il timeout di ritrasmissione aumenta in modo esponenziale per ogni ritrasmissione fino al valore massimo di 60sec e quindi rimane.</td>
</tr>
<tr>
<td>TCP_NODELAY</td>
<td>sì</td>
<td>sì</td>
<td>DWORD (booleano)</td>
<td>Abilita o Disabilita l'algoritmo Nagle per i socket TCP. Per impostazione predefinita, questa opzione è disabilitata (impostata su FALSE).</td>
</tr>
<tr>
<td>TCP_TIMESTAMPS</td>
<td>sì</td>
<td>sì</td>
<td>DWORD (booleano)</td>
<td>Abilita o Disabilita i timestamp RFC 1323. Si noti che è disponibile anche una configurazione globale per i timestamp (il valore predefinito è off), i &quot; timestamp &quot; in (set/get)-nettcpsetting. L'impostazione di questa opzione socket sostituisce l'impostazione di configurazione globale.</td>
</tr>
<tr>
<td>TCP_FASTOPEN</td>
<td>sì</td>
<td>sì</td>
<td>DWORD (booleano)</td>
<td>Abilita o Disabilita la <a href="https://tools.ietf.org/html/rfc7413">RFC 7413</a> TCP Fast Open, che consente di iniziare a inviare i dati durante la fase di handshake a tre vie di apertura di una connessione. Si noti che per usare l'apertura rapida, è necessario usare <a href="/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex"><strong>ConnectEx</strong></a> per stabilire la connessione iniziale e specificare i dati nel parametro <em>lpSendBuffer</em> della funzione da trasferire durante il processo di handshake. Alcuni dati in <em>lpSendBuffer</em> verranno trasferiti sotto il protocollo Fast Open.</td>
</tr>
<tr>
<td>TCP_KEEPIDLE</td>
<td>sì</td>
<td>sì</td>
<td>DWORD</td>
<td>Ottiene o imposta il numero di secondi durante i quali una connessione TCP rimarrà inattiva prima dell'invio di probe KeepAlive al computer remoto.
<blockquote>
[!Note]<br />
Questa opzione è disponibile a partire da Windows 10, versione 1709.
</blockquote>
<br/></td>
</tr>
<tr>
<td>TCP_KEEPINTVL</td>
<td>sì</td>
<td>sì</td>
<td>DWORD</td>
<td>Ottiene o imposta il numero di secondi durante i quali una connessione TCP resterà in attesa di una risposta KeepAlive prima di inviare un altro Probe KeepAlive.
<blockquote>
[!Note]<br />
Questa opzione è disponibile a partire da Windows 10, versione 1709.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>

## <a name="windows-support-for-ipproto_tcp-options"></a>Supporto di Windows per le \_ Opzioni TCP IPPROTO

| Opzione | Windows 10 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|
| \_BSDURGENT TCP | x | x | x | x |
| TCP \_ accelerato \_ 1122 | x | x | x | x |
| \_KEEPCNT TCP | A partire da Windows 10 versione 1703 | | | |
| \_MAXRT TCP | x | x | x | x |
| NoDelay TCP \_ | x | x | x | x |
| \_timestamp TCP | x | x | x | x |
| \_FASTOPEN TCP | A partire da Windows 10 versione 1607 | | | |

<br/>

 | Opzione | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/Me |
|-|-|-|-|-|-|
| \_BSDURGENT TCP | x | x | x | x | |
| TCP \_ accelerato \_ 1122 | x | x | x | | |
| \_KEEPCNT TCP | | | | | |
| \_MAXRT TCP | | | | | |
| NoDelay TCP \_ | x | x | x | x | |
| \_timestamp TCP | | | | | |
| \_FASTOPEN TCP | | | | | |

## <a name="remarks"></a>Commenti

In Microsoft Windows Software Development Kit (SDK) rilasciato per Windows Vista e versioni successive, l'organizzazione dei file di intestazione è stata modificata e il livello **\_ TCP IPPROTO** è definito nel file di intestazione *Ws2def. h* , che viene automaticamente incluso nel file di intestazione *Winsock2. h* . Le opzioni del socket **\_ TCP IPPROTO** , ad eccezione di **TCP \_ BSDURGENT**, sono definite nel file di intestazione *Ws2ipdef. h* , incluso automaticamente nel file di intestazione *Ws2tcpip. h* . L'opzione **TCP \_ BSDURGENT** per i motivi storici è definita nel file di intestazione *mswsock. h* . I file di intestazione *Ws2def. h* e *Ws2ipdef. h* non devono mai essere usati direttamente.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione | <dl> <dt>Ws2def. h (includere Winsock2. h); </dt> <dt>Winsock2. h in Windows Server 2003, Windows XP e windows 2000</dt> </dl> |
