---
description: Le tabelle seguenti descrivono le opzioni del socket IP IPPROTO che si applicano ai socket creati per la famiglia di indirizzi \_ IPv4 (AF \_ INET). Per altre informazioni su come ottenere e impostare le opzioni socket, vedere le pagine di riferimento sulle funzioni getsockopt e setsockopt.
ms.assetid: 6b06a29e-59cd-4446-bd2f-131dc25bf571
title: Opzioni socket IPPROTO_IP
ms.topic: article
ms.date: 10/02/2019
ms.openlocfilehash: 4ce469ab9989bc1cd3ec261e3d3a1b3b819c30443225fee24ae06c92efb6bace
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927711"
---
# <a name="ipproto_ip-socket-options"></a>Opzioni del \_ socket IPPROTO

Le tabelle seguenti **descrivono IPPROTO_IP** socket che si applicano ai socket creati per la famiglia di indirizzi IPv4 (AF \_ INET). Per altre informazioni su come ottenere e impostare le opzioni socket, vedere le pagine di riferimento sulle funzioni [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt.**](/windows/desktop/api/winsock/nf-winsock-setsockopt)

Per enumerare i protocolli e individuare le proprietà supportate per ogni protocollo installato, usare la funzione [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

Alcune opzioni socket richiedono una spiegazione maggiore di quanto possano comunicare queste tabelle. Tali opzioni contengono collegamenti a pagine aggiuntive.

## <a name="options"></a>Opzioni

| Opzione | Recupero | Impostazione | Tipo Optval | Descrizione |
|-|-|-|-|-|
| IP_ADD_IFLIST | | sì | DWORD (IF_INDEX) | Aggiunge un indice di interfaccia all'elenco IFLIST associato **all'IP_IFLIST** predefinita. |
| IP_ADD_MEMBERSHIP | | sì | [**ip_mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq) | Unire il socket al gruppo multicast fornito sull'interfaccia specificata. |
| IP_ADD_SOURCE_MEMBERSHIP | | sì | [**ip \_ mreq \_ source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Creare un join del gruppo multicast fornito sull'interfaccia specificata e accettare i dati provenienti dall'indirizzo di origine fornito. |
| ORIGINE \_ BLOCCO \_ IP | | sì | [**ip \_ mreq \_ source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Rimuove l'origine specificata come mittente dal gruppo multicast e dall'interfaccia forniti. |
| IP_DEL_IFLIST | | sì | DWORD (IF_INDEX) | Rimuove un indice di interfaccia dall'elenco IFLIST associato **all'IP_IFLIST** predefinita. Le voci possono essere rimosse solo dall'applicazione, quindi tenere presente che le voci potrebbero non essere più disponibili dopo la rimozione di un'interfaccia. |
| IP \_ DONTFRAGMENT | sì | sì | DWORD (booleano) | Indica che i dati non devono essere frammentati indipendentemente dall'MTU locale. Valido solo per i protocolli orientati ai messaggi. I provider TCP/IP Microsoft rispettano questa opzione per UDP e ICMP. |
| IP \_ DROP \_ MEMBERSHIP | | sì | [**ip \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq) | Lascia il gruppo multicast specificato dall'interfaccia specificata. I provider di servizi devono supportare questa opzione quando è supportato il multicast. Il supporto è indicato nella struttura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) restituita da una chiamata di funzione [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) con: XPI \_ SUPPORT \_ MULTIPOINT=1, XP1 \_ MULTIPOINT \_ CONTROL \_ PLANE=0, XP1 \_ MULTIPOINT DATA \_ \_ PLANE=0. |
| IP \_ DROP \_ SOURCE \_ MEMBERSHIP | | sì | [**ip \_ mreq \_ source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Elimina l'appartenenza al gruppo multicast, all'interfaccia e all'indirizzo di origine dati. |
| IP_GET_IFLIST | sì | | DWORD[] (IF_INDEX[]) | Ottiene l'oggetto IFLIST corrente associato **all'IP_IFLIST** predefinita. Restituisce un errore **se IP_IFLIST** non è abilitato. |
| IP \_ HDRINCL | sì | sì | DWORD (booleano) | Se impostato su **TRUE,** indica che l'applicazione fornisce l'intestazione IP. Si applica solo ai \_ socket RAW SOCK. Il provider di servizi TCP/IP può impostare il campo ID, se il valore fornito dall'applicazione è zero.  \_L'opzione IP HDRINCL viene applicata solo al tipo \_ di protocollo SOCK RAW. Un provider di servizi TCP/IP che supporta SOCK \_ RAW deve supportare anche IP \_ HDRINCL.  |
| IP_IFLIST | sì | sì | DWORD (booleano) | Ottiene o imposta lo **IP_IFLIST** del socket. Quando questa opzione è impostata su true, la ricezione del datagramma è limitata alle interfacce presenti in IFLIST. I datagrammi ricevuti in qualsiasi altra interfaccia vengono ignorati. IFLIST inizia vuoto. Usare **IP_ADD_IFLIST** e **IP_DEL_IFLIST** modificare l'ELENCO IFLIST. |
| IP \_ MTU | sì | | DWORD | Ottiene la stima del sistema del percorso MTU. Il socket deve essere connesso. |
| IP \_ MTU \_ DISCOVER | sì | sì | DWORD (**PMTUD \_ STATE**) | Ottiene o imposta lo stato di individuazione MTU del percorso per il socket. Il valore predefinito è **IP \_ PMTUDISC \_ NOT \_ SET.** Per i socket di flusso, **IP \_ PMTUDISC \_ NOT \_ SET** e **IP \_ PMTUDISC \_ DO** eseguiranno l'individuazione MTU del percorso. **IP \_ PMTUDISC \_ DONT** e **IP \_ PMTUDISC \_ PROBE** disattiva l'individuazione MTU del percorso. Per i socket di datagrammi, **IP \_ PMTUDISC \_ DO** forza tutti i pacchetti in uscita a impostare il bit DF e un tentativo di inviare pacchetti di dimensioni superiori al percorso MTU comporterà un errore. **IP \_ PMTUDISC \_ DONT forza** tutti i pacchetti in uscita a non impostare il bit DF e i pacchetti verranno frammentati in base all'interfaccia MTU. **IP \_ PMTUDISC \_ PROBE** forza l'impostazione del bit DF per tutti i pacchetti in uscita e un tentativo di inviare pacchetti di dimensioni superiori all'MTU dell'interfaccia comporterà un errore. |
| IP \_ MULTICAST \_ IF | sì | sì | DWORD | Ottiene o imposta l'interfaccia in uscita per l'invio del traffico multicast IPv4. Questa opzione non modifica l'interfaccia predefinita per la ricezione del traffico multicast IPv4.  Il valore di input per l'impostazione di questa opzione è un indirizzo IPv4 a 4 byte nell'ordine dei byte di rete. Questo parametro DWORD può anche essere un indice di interfaccia nell'ordine dei byte di rete. Qualsiasi indirizzo IP nel blocco 0.x.x.x (primo ottetto di 0) ad eccezione dell'indirizzo IPv4 0.0.0.0 viene considerato come un indice di interfaccia. Un indice di interfaccia è un numero a 24 bit e il blocco di indirizzi IPv4 0.0.0.0/8 non viene usato (questo intervallo è riservato). L'indice dell'interfaccia può essere usato per specificare l'interfaccia predefinita per il traffico multicast per IPv4. Se *optval è* zero, per l'invio del traffico multicast viene specificata l'interfaccia predefinita per la ricezione di multicast.  Quando si riceve questa opzione, *optval* restituisce l'indice di interfaccia predefinito corrente per l'invio del traffico IPv4 multicast nell'ordine dei byte dell'host. |
| CICLO \_ MULTICAST \_ IP | sì | sì | DWORD (booleano) | Controlla se i dati inviati da un'applicazione nel computer locale (non necessariamente dallo stesso socket) in una sessione multicast verranno ricevuti da un socket aggiunto al gruppo di destinazione multicast nell'interfaccia di loopback. Il valore **TRUE** fa sì che i dati multicast inviati da un'applicazione nel computer locale siano recapitati a un socket di ascolto nell'interfaccia di loopback. Il valore **FALSE impedisce** che i dati multicast inviati da un'applicazione nel computer locale vengano recapitati a un socket di ascolto nell'interfaccia di loopback. Per impostazione predefinita, **IP \_ MULTICAST \_ LOOPBACK** è abilitato. |
| IP \_ MULTICAST \_ TTL | sì | sì | DWORD | Imposta/ottiene il valore TTL associato al traffico multicast IP sul socket. |
| OPZIONI \_ IP | sì | sì | Char \[\] | Specifica le opzioni IP da inserire nei pacchetti in uscita. L'impostazione di nuove opzioni sovrascrive tutte le opzioni specificate in precedenza. Se si imposta optval su zero, vengono rimosse tutte le opzioni specificate in precedenza. Il supporto di OPZIONI IP non è necessario. Per verificare se OPZIONI IP è supportato, usare \_ \_ [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) per ottenere le opzioni correnti. Se **getsockopt ha esito** negativo, OPZIONI IP non è \_ supportato. |
| IP \_ ORIGINAL \_ ARRIVAL \_ IF | sì | sì | DWORD (booleano) | Indica se la funzione [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) deve restituire dati di controllo facoltativi contenenti l'interfaccia di arrivo in cui è stato ricevuto il pacchetto per i socket di datagrammi. Questa opzione consente all'interfaccia IPv4 in cui è stato ricevuto il pacchetto di essere restituita nella [**struttura WSAMSG.**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)  Questa opzione è valida solo per i datagrammi e i socket non elaborati (il tipo di socket deve essere SOCK \_ DGRAM o SOCK \_ RAW). |
| [IP \_ PKTINFO](ip-pktinfo.md) | sì | sì | DWORD | Indica che le informazioni sui pacchetti devono essere restituite dalla **funzione WSARecvMsg.** |
| TRASMISSIONE \_ DI RICEZIONE \_ IP | sì | sì | DWORD (booleano) | Consente o blocca la ricezione broadcast. |
| IP \_ RECVIF | sì | sì | DWORD (booleano) | Indica se lo stack IP deve popolare il buffer di controllo con i dettagli sull'interfaccia ricevuta da un pacchetto con un socket di datagramma. Quando questo valore è true, la funzione [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) restituirà dati di controllo facoltativi contenenti l'interfaccia in cui è stato ricevuto il pacchetto per i socket di datagrammi. Questa opzione consente all'interfaccia IPv4 in cui è stato ricevuto il pacchetto di essere restituita nella [**struttura WSAMSG.**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)  Questa opzione è valida solo per i datagrammi e i socket non elaborati (il tipo di socket deve essere SOCK \_ DGRAM o SOCK \_ RAW). |
| IP \_ RECVTOS | sì | sì | DWORD (booleano) | Indica se lo stack IP deve popolare il buffer di controllo con un messaggio contenente il campo di intestazione IPv4 Tipo di servizio (TOS) in un datagramma ricevuto. Quando questo valore è true, la funzione [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) restituirà dati di controllo facoltativi contenenti il valore del campo di intestazione TOS IPv4 del datagramma ricevuto.  Questa opzione consente di restituire il campo di intestazione TOS IPv4 del datagramma ricevuto nella [**struttura WSAMSG.**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) Il tipo di messaggio restituito sarà \_ TOS IP. Verranno restituiti tutti i bit DSCP ed ECN del campo TOS.  Questa opzione è valida solo nei socket di datagrammi (il tipo di socket deve essere SOCK \_ DGRAM).  |
| IP \_ RECVTTL | sì | sì | DWORD (booleano) | Indica che le informazioni sull'hop (TTL) devono essere restituite nella funzione [**LPFN_WSARECVMSG (WSARecvMsg).**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) Se *optval* è impostato su **1** nella chiamata a [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt), l'opzione è abilitata. Se impostata su **0,** l'opzione è disabilitata.  Questa opzione è valida solo per i datagrammi e i socket non elaborati (il tipo di socket deve essere SOCK \_ DGRAM o SOCK \_ RAW). |
| IP \_ TOS | sì | sì | DWORD (booleano) | Non usare. Le impostazioni del tipo di servizio (TOS) devono essere impostate solo usando l'API Quality of Service. Per [altre Differentiated Services,](/previous-versions/windows/desktop/qos/differentiated-services) vedere la sezione Relativa alla qualità del servizio di Platform SDK. |
| IP \_ TTL | sì | sì | DWORD (booleano) | Modifica il valore predefinito impostato dal provider di servizi TCP/IP nel campo TTL dell'intestazione IP nei datagrammi in uscita. Il supporto della durata (TTL IP) non è necessario. Per verificare se il TTL IP è supportato, usare \_ \_ [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) per ottenere le opzioni correnti. Se **getsockopt ha esito** negativo, il TTL IP non è \_ supportato. |
| ORIGINE \_ DI SBLOCCO \_ IP | | sì | [**ip \_ \_ mreq source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Aggiunge l'origine specificata come mittente al gruppo multicast e all'interfaccia forniti. |
| IP \_ UNICAST \_ IF | sì | sì | DWORD (INDICE \_ IF) | Ottiene o imposta l'interfaccia in uscita per l'invio del traffico IPv4. Questa opzione non modifica l'interfaccia predefinita per la ricezione del traffico IPv4. Questa opzione è importante per i computer multihomed.  Il valore di input per l'impostazione di questa opzione è un indirizzo IPv4 a 4 byte nell'ordine dei byte di rete. Questo parametro DWORD deve essere un indice di interfaccia nell'ordine dei byte di rete. Qualsiasi indirizzo IP nel blocco 0.x.x.x (primo ottetto di 0) ad eccezione dell'indirizzo IPv4 0.0.0.0 viene considerato come indice di interfaccia. Un indice di interfaccia è un numero a 24 bit e il blocco di indirizzi IPv4 0.0.0.0/8 non viene usato (questo intervallo è riservato). L'indice dell'interfaccia può essere usato per specificare l'interfaccia predefinita per l'invio del traffico per IPv4. La [**funzione GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) può essere usata per ottenere le informazioni sull'indice dell'interfaccia. Se *optval è* zero, l'interfaccia predefinita per l'invio del traffico è impostata su non specificata.  Quando si riceve questa opzione, *optval* restituisce l'indice di interfaccia predefinito corrente per l'invio del traffico IPv4 nell'ordine dei byte dell'host. |
| IP_USER_MTU | sì | sì | DWORD | Ottiene o imposta un limite superiore sul MTU del livello IP (in byte) per il socket specificato. Se il valore è superiore alla stima del sistema del percorso MTU (che è possibile recuperare in un socket connesso tramite una query sull'opzione socket **IP_MTU),** l'opzione non ha alcun effetto. Se il valore è inferiore, i pacchetti in uscita più grandi verranno frammentati o non verranno inviati, a seconda del valore **di IP_DONTFRAGMENT**. Il valore predefinito **è IP_UNSPECIFIED_USER_MTU** (MAXULONG). Per l'a protezione dei tipi, è consigliabile usare le funzioni [**WSAGetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) e [**WSASetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) anziché usare direttamente l'opzione socket. |
| CONTESTO DI \_ \_ REINDIRIZZAMENTO DELL'IP \_ PAM | sì | sì | WSACMSGHDR con dati di controllo | Tipo di dati accessorio del socket di datagramma (tipo cmsg) per indicare il contesto di reindirizzamento per un socket UDP utilizzato da un servizio di reindirizzamento della piattaforma di filtro di windows Windows(WFP) in \_ modalità utente. |
| RECORD DI \_ \_ REINDIRIZZAMENTO DELL'IP \_ PAM | sì | sì | WSACMSGHDR con dati di controllo | Tipo di dati di socket di datagramma (tipo cmsg) per indicare il record di reindirizzamento per un Windows socket UDP usato da un servizio di reindirizzamento della piattaforma di filtro dei dati (WFP) in modalità \_ utente. |

## <a name="windows-support-for-ip_proto-options"></a>Windows per le opzioni \_ PROTO IP

| Opzione | Windows 10 | Windows 8 | Windows Server 2012 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|-|-|
| IP_ADD_IFLIST | A partire Windows 10, versione 1803 | | | | | |
| IP \_ ADD \_ MEMBERSHIP | x | x | x | x | x | x |
| IP \_ ADD \_ SOURCE \_ MEMBERSHIP | x | x | x | x | x | x |
| ORIGINE \_ BLOCCO \_ IP | x | x | x | x | x | x |
| IP_DEL_IFLIST | A partire Windows 10, versione 1803 | | | | | |
| IP \_ DONTFRAGMENT | x | x | x | x | x | x |
| IP \_ DROP \_ MEMBERSHIP | x | x | x | x | x | x |
| IP \_ DROP \_ SOURCE \_ MEMBERSHIP | x | x | x | x | x | x |
| IP_GET_IFLIST | A partire Windows 10, versione 1803 | | | | | |
| IP \_ HDRINCL | x | x | x | x | x | x |
| IP_IFLIST | A partire Windows 10, versione 1803 | | | | | |
| IP \_ MULTICAST \_ IF | x | x | x | x | x | x |
| IP \_ MULTICAST \_ LOOP | x | x | x | x | x | x |
| IP \_ MULTICAST \_ TTL | x | x | x | x | x | x |
| OPZIONI \_ IP | x | x | x | x | x | x |
| ARRIVO \_ ORIGINALE \_ IP \_ SE | x | x | x | x | | |
| IP \_ PKTINFO | x | x | x | x | x | x |
| TRASMISSIONE \_ DI RICEZIONE \_ IP | x | x | x | x | x | x |
| IP \_ RECVIF | A partire da Windows 10, versione 1703 | x | x | x | x | x |
| IP \_ RECVTTL | x | | | | | |
| IP \_ TOS | x | x | x | | | |
| IP \_ TTL | x | x | x | x | x | x |
| ORIGINE \_ DI SBLOCCO \_ IP | x | x | x | x | x | x |
| IP \_ UNICAST \_ IF | x | x | x | x | x | x |
| CONTESTO \_ DI REINDIRIZZAMENTO DEL WFP \_ \_ IP | x | x | x | | | |
| RECORD \_ DI REINDIRIZZAMENTO DEL WFP \_ \_ IP | x | x | x | | | |

<br/>

| Opzione | Windows Server 2003 | Windows XP |
|-|-|-|
| IP_ADD_IFLIST | | |
| AGGIUNTA \_ \_ DELL'APPARTENENZA IP | x | x |
| AGGIUNTA \_ \_ DELL'APPARTENENZA \_ ALL'ORIGINE IP | x | x |
| ORIGINE \_ DEL BLOCCO \_ IP | x | x |
| IP_DEL_IFLIST | | |
| IP \_ DONTFRAGMENT | x | x |
| APPARTENENZA \_ ALL'ELIMINAZIONE \_ IP | x | x |
| APPARTENENZA \_ \_ ALL'ORIGINE DI RILASCIO \_ IP | x | x |
| IP_GET_IFLIST | | |
| IP \_ HDRINCL | x | x |
| IP_IFLIST | | |
| IP \_ MULTICAST \_ IF | x | x |
| CICLO \_ MULTICAST \_ IP | x | x |
| IP \_ MULTICAST \_ TTL | x | x |
| OPZIONI \_ IP | x | x |
| IP \_ ORIGINAL \_ ARRIVAL \_ IF | | |
| IP \_ PKTINFO | x | x |
| TRASMISSIONE \_ DI RICEZIONE \_ IP | x | x |
| IP \_ RECVIF | | |
| IP \_ RECVTTL | | |
| IP \_ TOS | | |
| IP \_ TTL | x | x |
| ORIGINE \_ DI SBLOCCO \_ IP | x | x |
| IP \_ UNICAST \_ IF | | |
| CONTESTO \_ DI REINDIRIZZAMENTO DEL WFP \_ \_ IP | | |
| RECORD \_ DI REINDIRIZZAMENTO DEL WFP \_ \_ IP | | |

## <a name="remarks"></a>Commenti

In Microsoft Windows Software Development Kit (SDK) rilasciato per Windows Vista e versioni successive, l'organizzazione dei file di intestazione è stata modificata e il livello **\_ IPPROTO** è definito nel file di intestazione *Ws2def.h* che viene incluso automaticamente nel file di *intestazione Winsock2.h.* Alcune delle opzioni del socket **\_ IPPROTO** sono definite nel file di intestazione *Ws2ipdef.h* incluso automaticamente dal file di intestazione *Ws2tcpip.h.* Le opzioni del socket **\_ IPPROTO** rimanenti sono definite nel file di intestazione *Wsipv6ok.h* che viene automaticamente incluso dal file di intestazione *Winsock2.h.* I file di intestazione *Ws2def.h*, *Ws2ipdef.h* e *Wsipv6ok.h* non devono mai essere usati direttamente.

In Platform SDK rilasciato per Windows Server 2003 e Windows XP, il livello **\_ IP IPPROTO** è definito nel file di intestazione *Winsock2.h.* Alcune delle opzioni del socket **\_ IPPROTO** sono definite nel file di intestazione *Ws2tcpip.h.* Le opzioni del socket **\_ IPPROTO** rimanenti sono definite nel file di intestazione *Wsipv6ok.h* che viene automaticamente incluso dal file di intestazione *Winsock2.h.* Il file *di intestazione Wsipv6ok.h* non deve mai essere usato direttamente.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione | <dl> <dt>Ws2def.h (includere Winsock2.h); </dt> <dt>Ws2ipdef.h (includere Ws2tcpip.h); </dt> <dt>Wsipv6ok.h (includere Winsock2.h)</dt> </dl> |
