---
description: Le tabelle seguenti descrivono le opzioni socket IPV6 IPPROTO che si applicano ai socket creati per la famiglia di indirizzi \_ IPv6 (AF \_ INET6). Per altre informazioni su come ottenere e impostare le opzioni socket, vedere le pagine di riferimento sulle funzioni getsockopt e setsockopt.
ms.assetid: 65f8f7a4-757b-43a3-9d47-b115754c89d6
title: Opzioni socket IPPROTO_IPV6
ms.topic: article
ms.date: 10/07/2019
ms.openlocfilehash: 0a6612e9d494325a40cf7b00803dbd13ead68def094383cb3faa50e0160ef932
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097751"
---
# <a name="ipproto_ipv6-socket-options"></a>Opzioni socket IPV6 IPPROTO \_

Le tabelle seguenti descrivono le opzioni socket **\_ IPV6 IPPROTO** che si applicano ai socket creati per la famiglia di indirizzi IPv6 (AF \_ INET6). Per altre informazioni su come ottenere e impostare le opzioni socket, vedere le pagine di riferimento sulle funzioni [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt.**](/windows/desktop/api/winsock/nf-winsock-setsockopt)

Per enumerare i protocolli e individuare le proprietà supportate per ogni protocollo installato, usare la funzione [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

Alcune opzioni socket richiedono una spiegazione maggiore di quanto possano comunicare queste tabelle. Tali opzioni contengono collegamenti a informazioni aggiuntive.

## <a name="options"></a>Opzioni

| Opzione | get | set | Tipo Optval | Descrizione |
|-|-|-|-|-|
| IP \_ ORIGINAL \_ ARRIVAL \_ IF | sì | sì | DWORD (booleano) | Indica se la [**funzione LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) deve restituire dati di controllo facoltativi contenenti l'interfaccia di arrivo originale in cui è stato ricevuto il pacchetto per i socket di datagramma. Questa opzione viene usata con tecnologie di transizione IPv6 (ad esempio tunnel 6to4, ISATAP e Teredo) che forniscono l'assegnazione di indirizzi e il tunneling automatico da host a host per il traffico IPv6 unicast quando gli host IPv6 devono attraversare le reti IP4 per raggiungere altre reti IPv6. I pacchetti IPv6 vengono inviati tramite tunnel come pacchetti IPv4. Questa opzione consente di restituire l'interfaccia IPv4 originale in cui è stato ricevuto il pacchetto nella [**struttura WSAMSG.**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)  |
| IPV6_ADD_IFLIST | | sì | DWORD (IF_INDEX) | Aggiunge un indice di interfaccia all'elenco IFLIST associato **all'IP_IFLIST** predefinita. |
| AGGIUNTA APPARTENENZA IPV6 \_ \_ | | sì | [**ipv6 \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Unire il socket al gruppo multicast fornito sull'interfaccia specificata.  Questa opzione è valida solo per i socket di datagramma e non elaborati (il tipo di socket deve essere SOCK \_ DGRAM o SOCK \_ RAW). |
| IPV6_DEL_IFLIST | | sì | DWORD (IF_INDEX) | Rimuove un indice di interfaccia dall'elenco IFLIST associato **all'IP_IFLIST** predefinita. Le voci possono essere rimosse solo dall'applicazione, quindi tenere presente che le voci potrebbero non essere più disponibili dopo la rimozione di un'interfaccia. |
| ELIMINAZIONE APPARTENENZA IPV6 \_ \_ | | sì | [**ipv6 \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Lasciare il gruppo multicast fornito dall'interfaccia specificata.  Questa opzione è valida solo per i socket di datagramma e non elaborati (il tipo di socket deve essere SOCK \_ DGRAM o SOCK \_ RAW). |
| IPV6_GET_IFLIST | sì | | DWORD[] (IF_INDEX[]) | Ottiene l'oggetto IFLIST corrente associato **all'IP_IFLIST** predefinita. Restituisce un errore **se IP_IFLIST** non è abilitato. |
| IPV6 \_ HDRINCL | sì | sì | DWORD(boolean) | Indica che l'applicazione fornisce l'intestazione IPv6 su tutti i dati in uscita. Se il *parametro optval* è impostato su **1** nella chiamata a [**setsockopt,**](/windows/desktop/api/winsock/nf-winsock-setsockopt)l'opzione è abilitata. Se *optval* è impostato su **0,** l'opzione è disabilitata. Il valore predefinito è Disattivata. Questa opzione è valida solo per i socket di datagramma e non elaborati (il tipo di socket deve essere SOCK \_ DGRAM o SOCK \_ RAW). Un provider di servizi TCP/IP che supporta SOCK \_ RAW deve supportare anche \_ HDRINCL IPV6. |
| IPV6 \_ HOPLIMIT | sì | sì | DWORD (booleano) | Indica che le informazioni sull'hop (TTL) devono essere restituite [**nella funzione LPFN_WSARECVMSG (WSARecvMsg).**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) Se *optval* è impostato su **1** nella chiamata a [**setsockopt,**](/windows/desktop/api/winsock/nf-winsock-setsockopt)l'opzione è abilitata. Se impostata su **0,** l'opzione è disabilitata.  Questa opzione è valida solo per i socket di datagramma e non elaborati (il tipo di socket deve essere SOCK \_ DGRAM o SOCK \_ RAW). |
| IPV6_IFLIST | sì | sì | DWORD (booleano) | Ottiene o imposta lo **IP_IFLIST** del socket. Quando questa opzione è impostata su true, la ricezione del datagramma è limitata alle interfacce presenti in IFLIST. I datagrammi ricevuti in qualsiasi altra interfaccia vengono ignorati. IFLIST inizia vuoto. Usare **IP_ADD_IFLIST** e **IP_DEL_IFLIST** per modificare l'ELENCO IFLIST. |
| GRUPPO DI JOIN IPV6 \_ \_ | | sì | [**ipv6 \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Uguale a IPV6 \_ ADD \_ MEMBERSHIP |
| GRUPPO DI LAVORO \_ IPV6 \_ | | sì | [**ipv6 \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) | Uguale a IPV6 \_ DROP \_ MEMBERSHIP |
| IPV6 \_ MTU | sì | | DWORD | Ottiene la stima del sistema del percorso MTU. Il socket deve essere connesso. |
| INDIVIDUAZIONE MTU IPV6 \_ \_ | sì | sì | DWORD (**PMTUD \_ STATE**) | Ottiene o imposta lo stato di individuazione MTU del percorso per il socket. Il valore predefinito è **IP \_ PMTUDISC \_ NOT \_ SET.** Per i socket di flusso, **IP \_ PMTUDISC \_ NOT \_ SET** e **IP \_ PMTUDISC \_ DO** eseguiranno l'individuazione MTU del percorso. **IP \_ PMTUDISC \_ DONT** e **IP \_ PMTUDISC \_ PROBE** disattiva l'individuazione MTU del percorso. Per i socket di datagrammi, se impostato su **IP \_ PMTUDISC \_ DO** , i tentativi di inviare pacchetti di dimensioni superiori al percorso MTU comporteranno un errore. Se impostato su **IP \_ PMTUDISC \_ DONT,** i pacchetti verranno frammentati in base all'interfaccia MTU. Se impostato su **IP \_ PMTUDISC \_ PROBE,** i tentativi di inviare pacchetti di dimensioni superiori a quelle dell'interfaccia MTU comporteranno un errore.  |
| \_HOP MULTICAST IPV6 \_ | sì | sì | DWORD | Ottiene o imposta il valore TTL associato al traffico multicast IPv6 nel socket. Non è valido impostare la durata (TTL) su un valore maggiore di 255.  Questa opzione è valida solo per i socket di datagramma e non elaborati (il tipo di socket deve essere SOCK \_ DGRAM o SOCK \_ RAW). |
| IPV6 \_ MULTICAST \_ IF | sì | sì | DWORD | Ottiene o imposta l'interfaccia in uscita per l'invio del traffico multicast IPv6. Questa opzione non modifica l'interfaccia predefinita per la ricezione del traffico multicast IPv6. Questa opzione è importante per i computer multihomed.  Il valore di input per l'impostazione di questa opzione è un indice di interfaccia a 4 byte dell'interfaccia in uscita desiderata nell'ordine dei byte dell'host. La [**funzione GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) può essere usata per ottenere le informazioni sull'indice dell'interfaccia. Se *optval* è impostato su **NULL** durante la chiamata a [**setsockopt,**](/windows/desktop/api/winsock/nf-winsock-setsockopt)viene usata l'interfaccia IPv6 predefinita. Se *optval è* zero, viene specificata l'interfaccia predefinita per la ricezione del multicast per l'invio del traffico multicast.  Quando si riceve questa opzione, *optval* restituisce l'indice di interfaccia predefinito corrente per l'invio del traffico IPv6 multicast nell'ordine dei byte dell'host. |
| CICLO MULTICAST IPV6 \_ \_ | sì | sì | DWORD (booleano) | Indica che i dati multicast inviati sul socket verranno inviati al buffer di ricezione dei socket se sono uniti anche nel gruppo multicast di destinazione. Se *optval* è impostato su **1** nella chiamata a [**setsockopt,**](/windows/desktop/api/winsock/nf-winsock-setsockopt)l'opzione è abilitata. Se impostata su **0,** l'opzione è disabilitata.  Questa opzione è valida solo per i socket di datagramma e non elaborati (il tipo di socket deve essere SOCK \_ DGRAM o SOCK \_ RAW). |
| [IPV6 \_ PKTINFO](ipv6-pktinfo.md) | sì | sì | DWORD (booleano) | Indica che le informazioni sui pacchetti devono essere restituite [**dalla LPFN_WSARECVMSG (WSARecvMsg).**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) |
| [LIVELLO DI PROTEZIONE IPV6 \_ \_](ipv6-protection-level.md) | sì | sì | INT | Abilita la restrizione di un socket a un ambito specificato, ad esempio indirizzi con lo stesso prefisso locale del collegamento o del sito. Fornisce vari livelli di restrizione e impostazioni predefinite. Per [altre informazioni, vedere LIVELLO \_ DI \_ PROTEZIONE IPV6.](ipv6-protection-level.md) |
| IPV6 \_ RECVIF | sì | sì | DWORD (booleano) | Indica se lo stack IP deve popolare il buffer di controllo con i dettagli sull'interfaccia che ha ricevuto un pacchetto con un socket di datagramma. Quando questo valore è true, la funzione [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) restituirà dati di controllo facoltativi contenenti l'interfaccia in cui è stato ricevuto il pacchetto per i socket di datagramma. Questa opzione consente all'interfaccia IPv6 in cui è stato ricevuto il pacchetto di essere restituita nella [**struttura WSAMSG.**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)  Questa opzione è valida solo per i socket di datagramma e non elaborati (il tipo di socket deve essere SOCK \_ DGRAM o SOCK \_ RAW). |
| IPV6 \_ RECVTCLASS | sì | sì | DWORD (booleano) | Indica se lo stack IP deve popolare il buffer di controllo con un messaggio contenente il campo di intestazione IPv6 della classe di traffico in un datagramma ricevuto. Quando questo valore è true, la funzione [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) restituirà dati di controllo facoltativi contenenti il valore del campo di intestazione IPv6 della classe di traffico del datagramma ricevuto.  Questa opzione consente di restituire il campo di intestazione IPv6 della classe di traffico del datagramma ricevuto nella [**struttura WSAMSG.**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) Il tipo di messaggio restituito sarà \_ TCLASS IPV6. Verranno restituiti tutti i bit DSCP ed ECN del campo Classe di traffico.  Questa opzione è valida solo nei socket di datagramma (il tipo di socket deve essere SOCK \_ DGRAM).  |
| \_HOP UNICAST IPV6 \_ | sì | sì | DWORD | Ottiene o imposta il valore TTL corrente associato al socket IPv6 per il traffico unicast. Non è valido impostare la durata (TTL) su un valore maggiore di 255. |
| IPV6 \_ UNICAST \_ IF | sì | sì | DWORD (IF \_ INDEX) | Ottiene o imposta l'interfaccia in uscita per l'invio del traffico IPv6. Questa opzione non modifica l'interfaccia predefinita per la ricezione del traffico IPv6. Questa opzione è importante per i computer multihomed.  Il valore di input per l'impostazione di questa opzione è un indice di interfaccia a 4 byte dell'interfaccia in uscita desiderata nell'ordine dei byte dell'host. La [**funzione GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) può essere usata per ottenere le informazioni sull'indice dell'interfaccia. Se *optval è* zero, l'interfaccia predefinita per l'invio del traffico IPv6 è impostata su non specificata.  Quando si riceve questa opzione, *optval* restituisce l'indice di interfaccia predefinito corrente per l'invio del traffico IPv6 nell'ordine dei byte dell'host. |
| IPV6_USER_MTU | sì | sì | DWORD | Ottiene o imposta un limite superiore sul MTU del livello IP (in byte) per il socket specificato. Se il valore è superiore alla stima del sistema del percorso MTU (che è possibile recuperare in un socket connesso tramite una query sull'opzione **socket IPV6_MTU),** l'opzione non ha alcun effetto. Se il valore è inferiore, i pacchetti in uscita più grandi verranno frammentati o non verranno inviati, a seconda del valore **di IPV6_DONTFRAG**. Il valore predefinito **è IP_UNSPECIFIED_USER_MTU** (MAXULONG). Per l'a protezione dei tipi, è consigliabile usare le funzioni [**WSAGetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) e [**WSASetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) anziché usare direttamente l'opzione socket. |
| IPV6 \_ V6ONLY | sì | sì | DWORD (booleano) | Indica se un socket creato per la famiglia di indirizzi \_ AF INET6 è limitato solo alle comunicazioni IPv6. I socket creati per la famiglia di indirizzi AF INET6 possono essere usati per \_ le comunicazioni IPv6 e IPv4. Alcune applicazioni potrebbero voler limitare l'uso di un socket creato per la famiglia di indirizzi \_ AF INET6 solo alle comunicazioni IPv6. Quando questo valore è diverso da zero (impostazione predefinita in Windows), un socket creato per la famiglia di indirizzi AF INET6 può essere usato solo per inviare e ricevere pacchetti \_ IPv6. Quando questo valore è zero, è possibile usare un socket creato per la famiglia di indirizzi AF INET6 per inviare e ricevere pacchetti da e verso un \_ indirizzo IPv6 o IPv4. Si noti che la possibilità di interagire con un indirizzo IPv4 richiede l'uso di indirizzi IPv4 mappati. Questa opzione socket è supportata in Windows Vista o versioni successive. |

## <a name="windows-support-for-ipproto_ipv6-socket-options"></a>Windows per le opzioni \_ socket IPV6 IPPROTO

| Opzione | Windows 8 | Windows Server 2012 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|-|
| IP \_ ORIGINAL \_ ARRIVAL \_ IF | x | x | x | | |
| IPV6_ADD_IFLIST | A partire da Windows 10, versione 1803 | | | | |
| AGGIUNTA APPARTENENZA IPV6 \_ \_ | x | x | x | x | x |
| IPV6_DEL_IFLIST | A partire da Windows 10, versione 1803 | | | | |
| APPARTENENZA DROP \_ IPV6 \_ | x | x | x | x | x |
| IPV6_GET_IFLIST | A partire da Windows 10, versione 1803 | | | | |
| IPV6 \_ HDRINCL | x | x | x | x | x |
| IPV6 \_ HOPLIMIT | x | x | x | x | x |
| IPV6_IFLIST | A partire da Windows 10, versione 1803 | | | | |
| GRUPPO DI JOIN IPV6 \_ \_ | x | x | x | x | x |
| GRUPPO LEAVE IPV6 \_ \_ | x | x | x | x | x |
| \_HOP MULTICAST IPV6 \_ | x | x | x | x | x |
| IPV6 \_ MULTICAST \_ IF | x | x | x | x | x |
| CICLO MULTICAST IPV6 \_ \_ | x | x | x | x | x |
| IPV6 \_ PKTINFO | x | x | x | x | x |
| [LIVELLO DI PROTEZIONE IPV6 \_ \_](ipv6-protection-level.md) | x | x | x | x | x |
| IPV6 \_ RECVIF | x | x | x | x | x |
| \_HOP UNICAST IPV6 \_ | x | x | x | x | x |
| IPV6 \_ UNICAST \_ IF | x | x | x | x | x |
| IPV6 \_ V6ONLY | x | x | x | x | x |

<br/>

| Opzione | Windows Server 2003 | Windows XP |
|-|-|-|
| IP \_ ORIGINAL \_ ARRIVAL \_ IF | | |
| IPV6_ADD_IFLIST | | |
| AGGIUNTA APPARTENENZA IPV6 \_ \_ | x | x |
| IPV6_DEL_IFLIST | | |
| APPARTENENZA DROP \_ IPV6 \_ | x | x |
| IPV6_GET_IFLIST | | |
| IPV6 \_ HDRINCL x | x |
| HOPLIMIT IPV6 \_ x | x |
| IPV6_IFLIST | | |
| GRUPPO DI JOIN IPV6 \_ \_ | x | x |
| GRUPPO LEAVE IPV6 \_ \_ | x | x |
| \_HOP MULTICAST IPV6 \_ | x | x |
| IPV6 \_ MULTICAST \_ IF | x | x |
| CICLO MULTICAST IPV6 \_ \_ | x | x |
| IPV6 \_ PKTINFO | x | x |
| [LIVELLO DI PROTEZIONE IPV6 \_ \_](ipv6-protection-level.md) | x | x |
| IPV6 \_ RECVIF | | |
| \_HOP UNICAST IPV6 \_ | x | x |
| IPV6 \_ UNICAST \_ IF | | |
| IPV6 \_ V6ONLY | | |

## <a name="remarks"></a>Commenti

In Microsoft Windows Software Development Kit (SDK) rilasciato per Windows Vista e versioni successive, l'organizzazione dei file di intestazione è stata modificata e il livello **\_ IPPROTO IPV6** è definito nel file di intestazione *Ws2def.h* incluso automaticamente nel file di intestazione *Winsock2.h.* Le opzioni del socket **\_ IPV6 IPPROTO** sono definite nel file di intestazione *Ws2ipdef.h* che viene automaticamente incluso nel file di intestazione *Ws2tcpip.h.* I *file di intestazione Ws2def.h* e *Ws2ipdef.h* non devono mai essere usati direttamente.

L'opzione socket IP ORIGINAL ARRIVAL IF è supportata \_ \_ in Windows Server \_ 2008 R2 e in Windows 7.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione | <dl> <dt>Ws2def.h (includere Winsock2.h);</dt> <dt>Winsock2.h in Windows Server 2003 e Windows XP</dt> </dl> |
