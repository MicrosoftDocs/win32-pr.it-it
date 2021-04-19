---
description: Le tabelle seguenti descrivono le \_ Opzioni del socket IP IPPROTO che si applicano ai socket creati per la famiglia di indirizzi IPv4 (AF \_ inet). Vedere le pagine di riferimento per le funzioni getsockopt e setsockopt per altre informazioni su come ottenere e impostare le opzioni del socket.
ms.assetid: 6b06a29e-59cd-4446-bd2f-131dc25bf571
title: Opzioni socket IPPROTO_IP
ms.topic: article
ms.date: 10/02/2019
ms.openlocfilehash: b4c8daa18e7bd60e61473bdda1c885bbd163f0b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326446"
---
# <a name="ipproto_ip-socket-options"></a>\_Opzioni del socket IP IPPROTO

Le tabelle seguenti descrivono le opzioni del socket **IPPROTO_IP** che si applicano ai socket creati per la famiglia di indirizzi IPv4 (AF \_ inet). Vedere le pagine di riferimento per le funzioni [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) per altre informazioni su come ottenere e impostare le opzioni del socket.

Per enumerare i protocolli e individuare le proprietà supportate per ogni protocollo installato, usare la funzione [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

Alcune opzioni del socket richiedono una spiegazione più che queste tabelle possono comportare; tali opzioni contengono collegamenti ad altre pagine.

## <a name="options"></a>Opzioni

| Opzione | Recupero | Set | Tipo optVal | Descrizione |
|-|-|-|-|-|
| IP_ADD_IFLIST | | sì | DWORD (IF_INDEX) | Aggiunge un indice di interfaccia a IFLIST associato all'opzione **IP_IFLIST** . |
| IP_ADD_MEMBERSHIP | | sì | [**ip_mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq) | Aggiungere il socket al gruppo multicast fornito nell'interfaccia specificata. |
| IP_ADD_SOURCE_MEMBERSHIP | | sì | [**\_origine MREQ \_ IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Aggiungere il gruppo multicast specificato sull'interfaccia specificata e accettare i dati originati dall'indirizzo di origine fornito. |
| \_origine blocco \_ IP | | sì | [**\_origine MREQ \_ IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Rimuove l'origine specificata come mittente per il gruppo multicast e l'interfaccia forniti. |
| IP_DEL_IFLIST | | sì | DWORD (IF_INDEX) | Rimuove un indice di interfaccia da IFLIST associato all'opzione **IP_IFLIST** . È possibile rimuovere le voci solo dall'applicazione, quindi tenere presente che le voci potrebbero non essere aggiornate dopo la rimozione di un'interfaccia. |
| \_DONTFRAGMENT IP | sì | sì | DWORD (booleano) | Indica che i dati non devono essere frammentati indipendentemente dall'MTU locale. Valido solo per i protocolli orientati ai messaggi. I provider Microsoft TCP/IP rispettano questa opzione per UDP e ICMP. |
| \_appartenenza a destinazione IP \_ | | sì | [**\_MREQ IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq) | Lascia il gruppo multicast specificato dall'interfaccia specificata. I provider di servizi devono supportare questa opzione quando il multicast è supportato. Il supporto è indicato nella struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) restituita da una chiamata di funzione [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) con i seguenti elementi: XPI \_ support \_ Multipoint = 1, XP1 \_ multipoint \_ Control \_ plane = 0, XP1 \_ multipoint \_ data \_ plane = 0. |
| \_ \_ appartenenza all'origine di eliminazione IP \_ | | sì | [**\_origine MREQ \_ IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Elimina l'appartenenza al gruppo multicast, all'interfaccia e all'indirizzo di origine specificati. |
| IP_GET_IFLIST | sì | | DWORD [] (IF_INDEX []) | Ottiene l'oggetto IFLIST corrente associato all'opzione **IP_IFLIST** . Restituisce un errore se **IP_IFLIST** non è abilitato. |
| \_HDRINCL IP | sì | sì | DWORD (booleano) | Se impostato su **true**, indica che l'applicazione fornisce l'intestazione IP. Si applica solo ai \_ socket raw Sock. Il provider di servizi TCP/IP può impostare il campo ID, se il valore fornito dall'applicazione è zero.  L' \_ opzione IP HDRINCL viene applicata solo al \_ tipo di protocollo di Sock RAW. Un provider di servizi TCP/IP che supporta SOCK \_ RAW deve supportare anche IP \_ HDRINCL.  |
| IP_IFLIST | sì | sì | DWORD (booleano) | Ottiene o imposta lo stato di **IP_IFLIST** del socket. Quando questa opzione è impostata su true, la ricezione del datagramma è limitata alle interfacce presenti in IFLIST. I datagrammi ricevuti su altre interfacce vengono ignorati. IFLIST viene avviato come vuoto. Usare **IP_ADD_IFLIST** e **IP_DEL_IFLIST** per modificare il IFLIST. |
| \_MTU IP | sì | | DWORD | Ottiene la stima del sistema dell'MTU del percorso. Il socket deve essere connesso. |
| \_individuazione MTU \_ IP | sì | sì | DWORD (**\_ stato il**) | Ottiene o imposta lo stato di individuazione MTU del percorso per il socket. Il valore predefinito è **IP \_ PMTUDISC \_ non \_ impostato**. Per i socket di flusso, **IP \_ PMTUDISC \_ non \_ impostato** e **IP \_ PMTUDISC \_ do** eseguiranno l'individuazione MTU del percorso. **Indirizzo IP \_ Il \_** **\_ \_ Probe** PMTUDISC dont e IP PMTUDISC disattiva il percorso MTU Discovery. Per i socket di datagramma, **IP \_ PMTUDISC \_** forza tutti i pacchetti in uscita affinché il bit DF sia impostato e un tentativo di inviare pacchetti di dimensioni maggiori di Path MTU provocherà un errore. **Indirizzo IP \_ PMTUDISC \_ dont** forza la mancata impostazione del bit DF per tutti i pacchetti in uscita e i pacchetti verranno frammentati in base al MTU di interfaccia. **Indirizzo IP \_ Il \_ Probe PMTUDISC** forza l'impostazione del bit DF per tutti i pacchetti in uscita e un tentativo di invio di pacchetti di dimensioni maggiori dell'interfaccia MTU genererà un errore. |
| \_multicast IP \_ se | sì | sì | DWORD | Ottiene o imposta l'interfaccia in uscita per l'invio del traffico multicast IPv4. Questa opzione non modifica l'interfaccia predefinita per la ricezione del traffico multicast IPv4.  Il valore di input per l'impostazione di questa opzione è un indirizzo IPv4 a 4 byte nell'ordine dei byte di rete. Questo parametro DWORD può essere anche un indice di interfaccia in ordine byte di rete. Qualsiasi indirizzo IP nel blocco 0. x. x.x. (primo ottetto di 0) ad eccezione dell'indirizzo IPv4 0.0.0.0 viene considerato come un indice di interfaccia. Un indice di interfaccia è un numero a 24 bit e il blocco di indirizzi IPv4 0.0.0.0/8 non viene utilizzato (questo intervallo è riservato). È possibile utilizzare l'indice dell'interfaccia per specificare l'interfaccia predefinita per il traffico multicast per IPv4. Se *optVal* è zero, l'interfaccia predefinita per la ricezione del multicast viene specificata per l'invio del traffico multicast.  Quando si recupera questa opzione, *optVal* restituisce l'indice dell'interfaccia predefinito corrente per l'invio del traffico IPv4 multicast nell'ordine dei byte dell'host. |
| \_ciclo multicast \_ IP | sì | sì | DWORD (booleano) | Controlla se i dati inviati da un'applicazione nel computer locale (non necessariamente dallo stesso socket) in una sessione multicast saranno ricevuti da un socket aggiunto al gruppo di destinazione multicast sull'interfaccia di loopback. Se il valore è **true** , i dati multicast inviati da un'applicazione nel computer locale vengono recapitati a un socket in ascolto sull'interfaccia di loopback. Il valore **false** impedisce che i dati multicast inviati da un'applicazione nel computer locale vengano recapitati a un socket in ascolto sull'interfaccia di loopback. Per impostazione predefinita, il **\_ \_ loopback multicast IP** è abilitato. |
| \_TTL multicast \_ IP | sì | sì | DWORD | Ottiene o imposta il valore TTL associato al traffico multicast IP nel socket. |
| \_opzioni IP | sì | sì | char \[\] | Specifica le opzioni IP da inserire nei pacchetti in uscita. L'impostazione di nuove opzioni sovrascrive tutte le opzioni specificate in precedenza. Se si imposta optVal su zero, verranno rimosse tutte le opzioni specificate in precedenza. Il \_ supporto delle opzioni IP non è necessario. per verificare se \_ sono supportate le opzioni IP, usare [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) per ottenere le opzioni correnti. Se **getsockopt** ha esito negativo, le \_ opzioni IP non sono supportate. |
| IP \_ originale \_ arrivo \_ se | sì | sì | DWORD (booleano) | Indica se la funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) deve restituire dati di controllo facoltativi contenenti l'interfaccia di arrivo in cui è stato ricevuto il pacchetto per i socket di datagramma. Questa opzione consente l'interfaccia IPv4 in cui è stato ricevuto il pacchetto da restituire nella struttura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) .  Questa opzione è valida solo su datagramma e socket RAW (il tipo di socket deve essere SOCK \_ DGRAM o Sock \_ RAW). |
| [\_pktinfo IP](ip-pktinfo.md) | sì | sì | DWORD | Indica che le informazioni sui pacchetti devono essere restituite dalla funzione **WSARecvMsg** . |
| \_trasmissione di ricezione IP \_ | sì | sì | DWORD (booleano) | Consente o blocca la ricezione broadcast. |
| \_RECVIF IP | sì | sì | DWORD (booleano) | Indica se lo stack IP deve popolare il buffer di controllo con i dettagli sull'interfaccia ricevuta da un pacchetto con un socket di datagramma. Quando questo valore è true, la funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) restituirà dati di controllo facoltativi contenenti l'interfaccia in cui è stato ricevuto il pacchetto per i socket di datagramma. Questa opzione consente l'interfaccia IPv4 in cui è stato ricevuto il pacchetto da restituire nella struttura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) .  Questa opzione è valida solo su datagramma e socket RAW (il tipo di socket deve essere SOCK \_ DGRAM o Sock \_ RAW). |
| \_RECVTOS IP | sì | sì | DWORD (booleano) | Indica se lo stack IP deve popolare il buffer di controllo con un messaggio contenente il campo di intestazione IPv4 del tipo di servizio (TOS) su un datagramma ricevuto. Quando questo valore è true, la funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) restituirà dati di controllo facoltativi contenenti il valore del campo di intestazione IPv4 TOS del datagramma ricevuto.  Questa opzione consente di restituire il campo di intestazione IPv4 TOS del datagramma ricevuto nella struttura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) . Il tipo di messaggio restituito sarà IP \_ TOS. Verranno restituiti tutti i bit DSCP e ECN del campo TOS.  Questa opzione è valida solo per i socket di datagramma (il tipo di socket deve essere SOCK \_ DGRAM).  |
| \_RECVTTL IP | sì | sì | DWORD (booleano) | Indica che le informazioni hop (TTL) devono essere restituite nella funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) . Se *optVal* è impostato su **1** nella chiamata a [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt), l'opzione è abilitata. Se impostato su **0**, l'opzione è disabilitata.  Questa opzione è valida solo per datagramma e socket RAW (il tipo di socket deve essere SOCK \_ DGRAM o Sock \_ RAW). |
| \_TOS IP | sì | sì | DWORD (booleano) | Non usare. Le impostazioni del tipo di servizio (TOS) devono essere impostate solo usando l'API di qualità del servizio. Per ulteriori informazioni, vedere [Servizi differenziati](/previous-versions/windows/desktop/qos/differentiated-services) nella sezione relativa alla qualità del servizio di Platform SDK. |
| \_TTL IP | sì | sì | DWORD (booleano) | Modifica il valore predefinito impostato dal provider di servizi TCP/IP nel campo TTL dell'intestazione IP nei datagrammi in uscita. Il \_ supporto IP TTL non è necessario. per verificare se \_ la durata IP è supportata, usare [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) per ottenere le opzioni correnti. Se **getsockopt** ha esito negativo, il valore \_ TTL IP non è supportato. |
| \_origine sblocco IP \_ | | sì | [**\_origine MREQ \_ IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) | Aggiunge l'origine specificata come mittente al gruppo e all'interfaccia multicast forniti. |
| \_unicast IP \_ se | sì | sì | DWORD (IF \_ index) | Ottiene o imposta l'interfaccia in uscita per l'invio del traffico IPv4. Questa opzione non modifica l'interfaccia predefinita per la ricezione del traffico IPv4. Questa opzione è importante per i computer multihomed.  Il valore di input per l'impostazione di questa opzione è un indirizzo IPv4 a 4 byte nell'ordine dei byte di rete. Questo parametro DWORD deve essere un indice di interfaccia in ordine byte di rete. Qualsiasi indirizzo IP nel blocco 0. x. x.x. (primo ottetto di 0) ad eccezione dell'indirizzo IPv4 0.0.0.0 viene considerato come un indice di interfaccia. Un indice di interfaccia è un numero a 24 bit e il blocco di indirizzi IPv4 0.0.0.0/8 non viene utilizzato (questo intervallo è riservato). È possibile utilizzare l'indice dell'interfaccia per specificare l'interfaccia predefinita per l'invio del traffico per IPv4. La funzione [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) può essere utilizzata per ottenere le informazioni sull'indice dell'interfaccia. Se *optVal* è zero, l'interfaccia predefinita per l'invio del traffico è impostata su Unspecified.  Quando si recupera questa opzione, *optVal* restituisce l'indice dell'interfaccia predefinito corrente per l'invio del traffico IPv4 nell'ordine dei byte dell'host. |
| IP_USER_MTU | sì | sì | DWORD | Ottiene o imposta un limite superiore sull'MTU del livello IP (in byte) per il socket specificato. Se il valore è superiore alla stima del sistema del valore MTU del percorso (che è possibile recuperare in un socket connesso eseguendo una query sull'opzione socket **IP_MTU** ), l'opzione non ha alcun effetto. Se il valore è inferiore, i pacchetti in uscita più grandi di questo verranno frammentati o non verranno inviati, a seconda del valore di **IP_DONTFRAGMENT**. Il valore predefinito è **IP_UNSPECIFIED_USER_MTU** (MAXULONG). Per indipendenza dai tipi, è consigliabile utilizzare le funzioni [**WSAGetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) e [**WSASetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) anziché utilizzare direttamente l'opzione socket. |
| \_contesto di \_ Reindirizzamento IP WFP \_ | sì | sì | WSACMSGHDR con dati di controllo | Tipo di dati ausiliario del socket del datagramma ( \_ tipo cmsg) per indicare il contesto di reindirizzamento per un socket UDP utilizzato da un servizio di reindirizzamento della modalità utente Windows Filtering Platform (WFP). |
| \_record di \_ Reindirizzamento IP WFP \_ | sì | sì | WSACMSGHDR con dati di controllo | Tipo di dati ausiliario del socket del datagramma ( \_ tipo cmsg) per indicare il record di reindirizzamento per un socket UDP usato da un servizio di reindirizzamento della modalità utente Windows Filtering Platform (WFP). |

## <a name="windows-support-for-ip_proto-options"></a>Supporto di Windows per le \_ opzioni IP proto

| Opzione | Windows 10 | Windows 8 | Windows Server 2012 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|-|-|
| IP_ADD_IFLIST | A partire da Windows 10 versione 1803 | | | | | |
| \_aggiunta \_ appartenenza IP | x | x | x | x | x | x |
| \_aggiunta di \_ \_ appartenenza all'origine IP | x | x | x | x | x | x |
| \_origine blocco \_ IP | x | x | x | x | x | x |
| IP_DEL_IFLIST | A partire da Windows 10 versione 1803 | | | | | |
| \_DONTFRAGMENT IP | x | x | x | x | x | x |
| \_appartenenza a destinazione IP \_ | x | x | x | x | x | x |
| \_ \_ appartenenza all'origine di eliminazione IP \_ | x | x | x | x | x | x |
| IP_GET_IFLIST | A partire da Windows 10 versione 1803 | | | | | |
| \_HDRINCL IP | x | x | x | x | x | x |
| IP_IFLIST | A partire da Windows 10 versione 1803 | | | | | |
| \_multicast IP \_ se | x | x | x | x | x | x |
| \_ciclo multicast \_ IP | x | x | x | x | x | x |
| \_TTL multicast \_ IP | x | x | x | x | x | x |
| \_opzioni IP | x | x | x | x | x | x |
| IP \_ originale \_ arrivo \_ se | x | x | x | x | | |
| \_pktinfo IP | x | x | x | x | x | x |
| \_trasmissione di ricezione IP \_ | x | x | x | x | x | x |
| \_RECVIF IP | A partire da Windows 10 versione 1703 | x | x | x | x | x |
| \_RECVTTL IP | x | | | | | |
| \_TOS IP | x | x | x | | | |
| \_TTL IP | x | x | x | x | x | x |
| \_origine sblocco IP \_ | x | x | x | x | x | x |
| \_unicast IP \_ se | x | x | x | x | x | x |
| \_contesto di \_ Reindirizzamento IP WFP \_ | x | x | x | | | |
| \_record di \_ Reindirizzamento IP WFP \_ | x | x | x | | | |

<br/>

| Opzione | Windows Server 2003 | Windows XP |
|-|-|-|
| IP_ADD_IFLIST | | |
| \_aggiunta \_ appartenenza IP | x | x |
| \_aggiunta di \_ \_ appartenenza all'origine IP | x | x |
| \_origine blocco \_ IP | x | x |
| IP_DEL_IFLIST | | |
| \_DONTFRAGMENT IP | x | x |
| \_appartenenza a destinazione IP \_ | x | x |
| \_ \_ appartenenza all'origine di eliminazione IP \_ | x | x |
| IP_GET_IFLIST | | |
| \_HDRINCL IP | x | x |
| IP_IFLIST | | |
| \_multicast IP \_ se | x | x |
| \_ciclo multicast \_ IP | x | x |
| \_TTL multicast \_ IP | x | x |
| \_opzioni IP | x | x |
| IP \_ originale \_ arrivo \_ se | | |
| \_pktinfo IP | x | x |
| \_trasmissione di ricezione IP \_ | x | x |
| \_RECVIF IP | | |
| \_RECVTTL IP | | |
| \_TOS IP | | |
| \_TTL IP | x | x |
| \_origine sblocco IP \_ | x | x |
| \_unicast IP \_ se | | |
| \_contesto di \_ Reindirizzamento IP WFP \_ | | |
| \_record di \_ Reindirizzamento IP WFP \_ | | |

## <a name="remarks"></a>Commenti

In Microsoft Windows Software Development Kit (SDK) rilasciato per Windows Vista e versioni successive, l'organizzazione dei file di intestazione è stata modificata e il livello **\_ IP IPPROTO** è definito nel file di intestazione *Ws2def. h* , che viene automaticamente incluso nel file di intestazione *Winsock2. h* . Alcune delle opzioni del socket **\_ IP di IPPROTO** sono definite nel file di intestazione *Ws2ipdef. h* , che viene automaticamente incluso nel file di intestazione *Ws2tcpip. h* . Le restanti opzioni del socket **\_ IP IPPROTO** sono definite nel file di intestazione *Wsipv6ok. h* , che viene automaticamente incluso nel file di intestazione *Winsock2. h* . I file di intestazione *Ws2def. h*, *Ws2ipdef. h* e *Wsipv6ok. h* non devono mai essere usati direttamente.

In Platform SDK rilasciato per Windows Server 2003 e Windows XP, il livello **\_ IP IPPROTO** è definito nel file di intestazione *Winsock2. h* . Alcune delle opzioni del socket **\_ IP di IPPROTO** sono definite nel file di intestazione *Ws2tcpip. h* . Le restanti opzioni del socket **\_ IP IPPROTO** sono definite nel file di intestazione *Wsipv6ok. h* , che viene automaticamente incluso nel file di intestazione *Winsock2. h* . Il file di intestazione *Wsipv6ok. h* non deve mai essere utilizzato direttamente.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione | <dl> <dt>Ws2def. h (includere Winsock2. h); </dt> <dt>Ws2ipdef. h (includere Ws2tcpip. h); </dt> <dt>Wsipv6ok. h (include Winsock2. h)</dt> </dl> |
