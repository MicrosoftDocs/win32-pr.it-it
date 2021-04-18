---
description: Le tabelle seguenti descrivono le \_ opzioni socket IPv6 di IPPROTO che si applicano ai socket creati per la famiglia di indirizzi IPv6 (AF \_ INET6). Vedere le pagine di riferimento per le funzioni getsockopt e setsockopt per altre informazioni su come ottenere e impostare le opzioni del socket.
ms.assetid: 65f8f7a4-757b-43a3-9d47-b115754c89d6
title: Opzioni socket IPPROTO_IPV6
ms.topic: article
ms.date: 10/07/2019
ms.openlocfilehash: 1ceaf08c2a59a24b9ff694ac9ff42b28fbf18480
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327135"
---
# <a name="ipproto_ipv6-socket-options"></a>\_Opzioni socket IPv6 IPPROTO

Le tabelle seguenti descrivono le opzioni socket **\_ IPv6 di IPPROTO** che si applicano ai socket creati per la famiglia di indirizzi IPv6 (AF \_ INET6). Vedere le pagine di riferimento per le funzioni [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) per altre informazioni su come ottenere e impostare le opzioni del socket.

Per enumerare i protocolli e individuare le proprietà supportate per ogni protocollo installato, usare la funzione [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

Alcune opzioni del socket richiedono una spiegazione più che queste tabelle possono comportare; tali opzioni contengono collegamenti a informazioni aggiuntive.

## <a name="options"></a>Opzioni

| Opzione | get | set | Tipo optVal | Descrizione |
|-|-|-|-|-|
| IP \_ originale \_ arrivo \_ se | sì | sì | DWORD (booleano) | Indica se la funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) deve restituire dati di controllo facoltativi contenenti l'interfaccia di arrivo originale in cui è stato ricevuto il pacchetto per i socket di datagramma. Questa opzione viene utilizzata con le tecnologie di transizione IPv6 (ad esempio, tunnel 6to4, ISATAP e Teredo) che forniscono l'assegnazione degli indirizzi e il tunneling automatico da host a host per il traffico IPv6 unicast quando gli host IPv6 devono attraversare le reti IP4 per raggiungere altre reti IPv6. I pacchetti IPv6 vengono inviati tramite tunnel come pacchetti IPv4. Questa opzione consente l'interfaccia IPv4 originale in cui è stato ricevuto il pacchetto da restituire nella struttura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) .  |
| IPV6_ADD_IFLIST | | sì | DWORD (IF_INDEX) | Aggiunge un indice di interfaccia a IFLIST associato all'opzione **IP_IFLIST** . |
| \_Aggiunta di \_ appartenenza a IPv6 | | sì | [**\_MREQ IPv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Aggiungere il socket al gruppo multicast fornito nell'interfaccia specificata.  Questa opzione è valida solo su datagramma e socket RAW (il tipo di socket deve essere SOCK \_ DGRAM o Sock \_ RAW). |
| IPV6_DEL_IFLIST | | sì | DWORD (IF_INDEX) | Rimuove un indice di interfaccia da IFLIST associato all'opzione **IP_IFLIST** . È possibile rimuovere le voci solo dall'applicazione, quindi tenere presente che le voci potrebbero non essere aggiornate dopo la rimozione di un'interfaccia. |
| \_Appartenenza a eliminazione IPv6 \_ | | sì | [**\_MREQ IPv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Lasciare il gruppo multicast fornito dall'interfaccia specificata.  Questa opzione è valida solo su datagramma e socket RAW (il tipo di socket deve essere SOCK \_ DGRAM o Sock \_ RAW). |
| IPV6_GET_IFLIST | sì | | DWORD [] (IF_INDEX []) | Ottiene l'oggetto IFLIST corrente associato all'opzione **IP_IFLIST** . Restituisce un errore se **IP_IFLIST** non è abilitato. |
| \_HDRINCL IPv6 | sì | sì | DWORD (booleano) | Indica che l'applicazione fornisce l'intestazione IPv6 su tutti i dati in uscita. Se il parametro *optVal* è impostato su **1** nella chiamata a [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt), l'opzione è abilitata. Se *optVal* è impostato su **0**, l'opzione è disabilitata. Il valore predefinito è Disattivata. Questa opzione è valida solo per datagramma e socket RAW (il tipo di socket deve essere SOCK \_ DGRAM o Sock \_ RAW). Un provider di servizi TCP/IP che supporta SOCK \_ RAW deve supportare anche IPv6 \_ HDRINCL. |
| \_HOPLIMIT IPv6 | sì | sì | DWORD (booleano) | Indica che le informazioni hop (TTL) devono essere restituite nella funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) . Se *optVal* è impostato su **1** nella chiamata a [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt), l'opzione è abilitata. Se impostato su **0**, l'opzione è disabilitata.  Questa opzione è valida solo per datagramma e socket RAW (il tipo di socket deve essere SOCK \_ DGRAM o Sock \_ RAW). |
| IPV6_IFLIST | sì | sì | DWORD (booleano) | Ottiene o imposta lo stato di **IP_IFLIST** del socket. Quando questa opzione è impostata su true, la ricezione del datagramma è limitata alle interfacce presenti in IFLIST. I datagrammi ricevuti su altre interfacce vengono ignorati. IFLIST viene avviato come vuoto. Usare **IP_ADD_IFLIST** e **IP_DEL_IFLIST** per modificare il IFLIST. |
| \_Gruppo join \_ IPv6 | | sì | [**\_MREQ IPv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Uguale a IPV6 \_ Aggiungi \_ appartenenza |
| \_Gruppo di uscita IPv6 \_ | | sì | [**\_MREQ IPv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Uguale \_ \_ all'appartenenza all'eliminazione IPv6 |
| \_MTU IPv6 | sì | | DWORD | Ottiene la stima del sistema dell'MTU del percorso. Il socket deve essere connesso. |
| \_Individuazione MTU \_ IPv6 | sì | sì | DWORD (**\_ stato il**) | Ottiene o imposta lo stato di individuazione MTU del percorso per il socket. Il valore predefinito è **IP \_ PMTUDISC \_ non \_ impostato**. Per i socket di flusso, **IP \_ PMTUDISC \_ non \_ impostato** e **IP \_ PMTUDISC \_ do** eseguiranno l'individuazione MTU del percorso. **Indirizzo IP \_ Il \_** **\_ \_ Probe** PMTUDISC dont e IP PMTUDISC disattiva il percorso MTU Discovery. Per i socket di datagramma, se impostati su **IP \_ PMTUDISC \_** , i tentativi di inviare pacchetti di dimensioni maggiori di Path MTU genereranno un errore. Se impostato su **IP \_ PMTUDISC \_ dont**, i pacchetti verranno frammentati in base all'MTU dell'interfaccia. Se è impostato **su \_ \_ Probe IP PMTUDISC**, i tentativi di inviare pacchetti di dimensioni superiori a quelle dell'interfaccia MTU genereranno un errore.  |
| \_Hop multicast \_ IPv6 | sì | sì | DWORD | Ottiene o imposta il valore TTL associato al traffico multicast IPv6 sul socket. Non è consentito impostare la durata (TTL) su un valore maggiore di 255.  Questa opzione è valida solo per datagramma e socket RAW (il tipo di socket deve essere SOCK \_ DGRAM o Sock \_ RAW). |
| \_Multicast IPv6 \_ se | sì | sì | DWORD | Ottiene o imposta l'interfaccia in uscita per l'invio del traffico multicast IPv6. Questa opzione non modifica l'interfaccia predefinita per la ricezione del traffico multicast IPv6. Questa opzione è importante per i computer multihomed.  Il valore di input per l'impostazione di questa opzione è un indice di interfaccia a 4 byte dell'interfaccia in uscita desiderata nell'ordine dei byte dell'host. La funzione [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) può essere utilizzata per ottenere le informazioni sull'indice dell'interfaccia. Se *optVal* è impostato su **null** nella chiamata a [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt), viene utilizzata l'interfaccia IPv6 predefinita. Se *optVal* è zero, l'interfaccia predefinita per la ricezione del multicast viene specificata per l'invio del traffico multicast.  Quando si recupera questa opzione, *optVal* restituisce l'indice dell'interfaccia predefinito corrente per l'invio del traffico IPv6 multicast nell'ordine dei byte dell'host. |
| \_Ciclo multicast \_ IPv6 | sì | sì | DWORD (booleano) | Indica che i dati multicast inviati sul socket verranno restituiti al buffer di ricezione dei socket se è stato aggiunto anche al gruppo multicast di destinazione. Se *optVal* è impostato su **1** nella chiamata a [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt), l'opzione è abilitata. Se impostato su **0**, l'opzione è disabilitata.  Questa opzione è valida solo per datagramma e socket RAW (il tipo di socket deve essere SOCK \_ DGRAM o Sock \_ RAW). |
| [\_Pktinfo IPv6](ipv6-pktinfo.md) | sì | sì | DWORD (booleano) | Indica che le informazioni sui pacchetti devono essere restituite dalla funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) . |
| [\_Livello di protezione IPv6 \_](ipv6-protection-level.md) | sì | sì | INT | Consente la restrizione di un socket a un ambito specificato, ad esempio indirizzi con lo stesso prefisso locale del collegamento o del sito. In sono disponibili diversi livelli di restrizione e impostazioni predefinite. Per ulteriori informazioni, vedere [ \_ \_ livello di protezione IPv6](ipv6-protection-level.md) . |
| \_RECVIF IPv6 | sì | sì | DWORD (booleano) | Indica se lo stack IP deve popolare il buffer di controllo con i dettagli sull'interfaccia ricevuta da un pacchetto con un socket di datagramma. Quando questo valore è true, la funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) restituirà dati di controllo facoltativi contenenti l'interfaccia in cui è stato ricevuto il pacchetto per i socket di datagramma. Questa opzione consente l'interfaccia IPv6 in cui è stato ricevuto il pacchetto da restituire nella struttura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) .  Questa opzione è valida solo per datagramma e socket RAW (il tipo di socket deve essere SOCK \_ DGRAM o Sock \_ RAW). |
| \_RECVTCLASS IPv6 | sì | sì | DWORD (booleano) | Indica se lo stack IP deve popolare il buffer di controllo con un messaggio contenente il campo di intestazione IPv6 della classe di traffico su un datagramma ricevuto. Quando questo valore è true, la funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) restituirà dati di controllo facoltativi contenenti il valore del campo di intestazione IPv6 della classe di traffico del datagramma ricevuto.  Questa opzione consente la restituzione del campo di intestazione IPv6 della classe Traffic del datagramma ricevuto nella struttura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) . Il tipo di messaggio restituito sarà \_ TCLASS IPv6. Verranno restituiti tutti i bit DSCP e ECN del campo della classe di traffico.  Questa opzione è valida solo per i socket di datagramma (il tipo di socket deve essere SOCK \_ DGRAM).  |
| \_Hop unicast \_ IPv6 | sì | sì | DWORD | Ottiene o imposta il valore TTL corrente associato al socket IPv6 per il traffico unicast. Non è consentito impostare la durata (TTL) su un valore maggiore di 255. |
| \_Unicast IPv6 \_ se | sì | sì | DWORD (IF \_ index) | Ottiene o imposta l'interfaccia in uscita per l'invio del traffico IPv6. Questa opzione non consente di modificare l'interfaccia predefinita per la ricezione del traffico IPv6. Questa opzione è importante per i computer multihomed.  Il valore di input per l'impostazione di questa opzione è un indice di interfaccia a 4 byte dell'interfaccia in uscita desiderata nell'ordine dei byte dell'host. La funzione [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) può essere utilizzata per ottenere le informazioni sull'indice dell'interfaccia. Se *optVal* è zero, l'interfaccia predefinita per l'invio del traffico IPv6 è impostata su Unspecified.  Quando si recupera questa opzione, *optVal* restituisce l'indice dell'interfaccia predefinito corrente per l'invio del traffico IPv6 nell'ordine dei byte dell'host. |
| IPV6_USER_MTU | sì | sì | DWORD | Ottiene o imposta un limite superiore sull'MTU del livello IP (in byte) per il socket specificato. Se il valore è superiore alla stima del sistema del valore MTU del percorso (che è possibile recuperare in un socket connesso eseguendo una query sull'opzione socket **IPV6_MTU** ), l'opzione non ha alcun effetto. Se il valore è inferiore, i pacchetti in uscita più grandi di questo verranno frammentati o non verranno inviati, a seconda del valore di **IPV6_DONTFRAG**. Il valore predefinito è **IP_UNSPECIFIED_USER_MTU** (MAXULONG). Per indipendenza dai tipi, è consigliabile utilizzare le funzioni [**WSAGetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) e [**WSASetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) anziché utilizzare direttamente l'opzione socket. |
| \_V6ONLY IPv6 | sì | sì | DWORD (booleano) | Indica se un socket creato per la \_ famiglia di indirizzi AF INET6 è limitato solo alle comunicazioni IPv6. I socket creati per la \_ famiglia di indirizzi AF INET6 possono essere usati per le comunicazioni IPv6 e IPv4. Alcune applicazioni potrebbero voler limitare l'uso di un socket creato per la \_ famiglia di indirizzi INET6 AF solo alle comunicazioni IPv6. Quando questo valore è diverso da zero (impostazione predefinita in Windows), è possibile usare un socket creato per la \_ famiglia di indirizzi INET6 AF per inviare e ricevere solo pacchetti IPv6. Quando questo valore è zero, un socket creato per la \_ famiglia di indirizzi AF INET6 può essere usato per inviare e ricevere pacchetti da e verso un indirizzo IPv6 o un indirizzo IPv4. Si noti che la possibilità di interagire con un indirizzo IPv4 richiede l'uso di indirizzi IPv4 mappati. Questa opzione socket è supportata in Windows Vista o versioni successive. |

## <a name="windows-support-for-ipproto_ipv6-socket-options"></a>Supporto di Windows per le \_ opzioni socket IPv6 IPPROTO

| Opzione | Windows 8 | Windows Server 2012 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|-|
| IP \_ originale \_ arrivo \_ se | x | x | x | | |
| IPV6_ADD_IFLIST | A partire da Windows 10 versione 1803 | | | | | |
| \_Aggiunta di \_ appartenenza a IPv6 | x | x | x | x | x |
| IPV6_DEL_IFLIST | A partire da Windows 10 versione 1803 | | | | | |
| \_Appartenenza a eliminazione IPv6 \_ | x | x | x | x | x |
| IPV6_GET_IFLIST | A partire da Windows 10 versione 1803 | | | | | |
| \_HDRINCL IPv6 | x | x | x | x | x |
| \_HOPLIMIT IPv6 | x | x | x | x | x |
| IPV6_IFLIST | A partire da Windows 10 versione 1803 | | | | | |
| \_Gruppo join \_ IPv6 | x | x | x | x | x |
| \_Gruppo di uscita IPv6 \_ | x | x | x | x | x |
| \_Hop multicast \_ IPv6 | x | x | x | x | x |
| \_Multicast IPv6 \_ se | x | x | x | x | x |
| \_Ciclo multicast \_ IPv6 | x | x | x | x | x |
| \_Pktinfo IPv6 | x | x | x | x | x |
| [\_Livello di protezione IPv6 \_](ipv6-protection-level.md) | x | x | x | x | x |
| \_RECVIF IPv6 | x | x | x | x | x |
| \_Hop unicast \_ IPv6 | x | x | x | x | x |
| \_Unicast IPv6 \_ se | x | x | x | x | x |
| \_V6ONLY IPv6 | x | x | x | x | x |

<br/>

| Opzione | Windows Server 2003 | Windows XP |
|-|-|-|
| IP \_ originale \_ arrivo \_ se | | |
| IPV6_ADD_IFLIST | | |
| \_Aggiunta di \_ appartenenza a IPv6 | x | x |
| IPV6_DEL_IFLIST | | |
| \_Appartenenza a eliminazione IPv6 \_ | x | x |
| IPV6_GET_IFLIST | | |
| \_HDRINCL IPv6 x | x |
| \_HOPLIMIT IPv6 x | x |
| IPV6_IFLIST | | |
| \_Gruppo join \_ IPv6 | x | x |
| \_Gruppo di uscita IPv6 \_ | x | x |
| \_Hop multicast \_ IPv6 | x | x |
| \_Multicast IPv6 \_ se | x | x |
| \_Ciclo multicast \_ IPv6 | x | x |
| \_Pktinfo IPv6 | x | x |
| [\_Livello di protezione IPv6 \_](ipv6-protection-level.md) | x | x |
| \_RECVIF IPv6 | | |
| \_Hop unicast \_ IPv6 | x | x |
| \_Unicast IPv6 \_ se | | |
| \_V6ONLY IPv6 | | |

## <a name="remarks"></a>Commenti

In Microsoft Windows Software Development Kit (SDK) rilasciato per Windows Vista e versioni successive, l'organizzazione dei file di intestazione è stata modificata e il livello **\_ IPv6 di IPPROTO** è definito nel file di intestazione *Ws2def. h* , che viene automaticamente incluso nel file di intestazione *Winsock2. h* . Le opzioni del socket **\_ IPv6 IPPROTO** sono definite nel file di intestazione *Ws2ipdef. h* , che viene automaticamente incluso nel file di intestazione *Ws2tcpip. h* . I file di intestazione *Ws2def. h* e *Ws2ipdef. h* non devono mai essere usati direttamente.

L' \_ \_ opzione socket IP Original arrival \_ If è supportata in Windows Server 2008 R2 e in Windows 7.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione | <dl> <dt>Ws2def. h (includere Winsock2. h); </dt> <dt>Winsock2. h in Windows Server 2003 e Windows XP</dt> </dl> |
