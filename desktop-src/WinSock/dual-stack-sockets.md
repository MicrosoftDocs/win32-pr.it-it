---
description: Per supportare sia IPv4 che IPv6 in Windows XP con Service Pack 1 (SP1) e in Windows Server 2003, un'applicazione deve creare due socket, uno da usare con IPv4 e uno per l'uso con IPv6.
ms.assetid: 7ae49081-ffb5-4eee-b488-2541398e7acc
title: Dual-Stack socket per applicazioni Winsock IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424580569fb3bed5e81c6232cb99dc2d53a30af1ab2c23c9b4afa6945c0a6eb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132664"
---
# <a name="dual-stack-sockets-for-ipv6-winsock-applications"></a>Dual-Stack socket per applicazioni Winsock IPv6

Per supportare sia IPv4 che IPv6 in Windows XP con Service Pack 1 (SP1) e in Windows Server 2003, un'applicazione deve creare due socket, uno da usare con IPv4 e uno per l'uso con IPv6. Questi due socket devono essere gestiti separatamente dall'applicazione.

Windows Vista e versioni successive offrono la possibilità di creare un singolo socket IPv6 in grado di gestire sia il traffico IPv6 che il traffico IPv4. Ad esempio, viene creato un socket di ascolto TCP per IPv6, inserito in modalità dual stack e associato alla porta 5001. Questo socket dual stack può accettare connessioni dai client TCP IPv6 che si connettono alla porta 5001 e dai client TCP IPv4 che si connettono alla porta 5001. Questa funzionalità consente di semplificare notevolmente la progettazione delle applicazioni e riduce il sovraccarico delle risorse necessario per l'inserimento di operazioni su due socket separati.

## <a name="creating-a-dual-stack-socket"></a>Creazione di un socket Dual-Stack

Per impostazione predefinita, un socket IPv6 creato Windows Vista e versioni successive funziona solo tramite il protocollo IPv6. Per rendere un socket IPv6 in un socket dual stack, è necessario chiamare la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) con l'opzione socket **IPV6 \_ V6ONLY** per impostare questo valore su zero prima che il socket venga associato a un indirizzo IP. Quando **l'opzione socket IPV6 \_ V6ONLY** è impostata su zero, è possibile usare un socket creato per la famiglia di indirizzi **AF \_ INET6** per inviare e ricevere pacchetti da e verso un indirizzo IPv6 o un indirizzo mappato IPv4.

## <a name="ip-addresses-with-a-dual-stack-socket"></a>Indirizzi IP con un socket Dual-Stack

I socket dual stack richiedono sempre indirizzi IPv6. La possibilità di interagire con un indirizzo IPv4 richiede l'uso del formato di indirizzo IPv6 mappato a IPv4. Tutti gli indirizzi IPv4 devono essere rappresentati nel formato di indirizzo IPv6 mappato a IPv4, che consente a un'applicazione solo IPv6 di comunicare con un nodo IPv4. Il formato di indirizzo IPv6 mappato a IPv4 consente di rappresentare l'indirizzo IPv4 di un nodo IPv4 come indirizzo IPv6. L'indirizzo IPv4 viene codificato nei 32 bit meno elevati dell'indirizzo IPv6 e i 96 bit più alti contengono il prefisso fisso 0:0:0:0:0:FFFF. Il formato di indirizzo IPv6 mappato a IPv4 è specificato in RFC 4291. Per altre informazioni, vedere [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291). La macro IN6ADDR \_ SETV4MAPPED in *Mstcpip.h* può essere usata per convertire un indirizzo IPv4 nel formato di indirizzo IPv6 mappato a IPv4 richiesto.

Se il protocollo sottostante è effettivamente IPv4, l'indirizzo IPv4 viene mappato in un formato di indirizzo IPv6 mappato a IPv4. Il campo family nella struttura [SOCKADDR](sockaddr-2.md) indica AF INET6, ma un indirizzo IPv6 mappato a IPv4 viene codificato nella struttura degli indirizzi \_ IPv6. Per un socket dual stack in modalità di ascolto, ciò significa che tutte le connessioni IPv4 accettate restituiranno un indirizzo IPv6 mappato a IPv4. Per un socket dual stack che si connette a una destinazione IPv4, la struttura SOCKADDR passata per la connessione deve essere un indirizzo IPv6 mappato a IPv4. Le applicazioni devono gestire questi indirizzi IPv6 mappati a IPv4 in modo appropriato e usarli solo con socket dual stack. Se un indirizzo IP deve essere passato a un normale socket IPv4, l'indirizzo deve essere un indirizzo IPv4 normale e non un indirizzo IPv6 mappato a IPv4.

## <a name="potential-issues-using-a-dual-stack-socket"></a>Potenziali problemi di utilizzo di un socket Dual-Stack

Un potenziale problema per le applicazioni è il recupero di un indirizzo IPv6 mappato a IPv4 in un socket dual stack e il tentativo di usare l'indirizzo IP restituito in un socket solo IPv6 diverso. Ad esempio, le [**funzioni getsockname**](/windows/desktop/api/winsock/nf-winsock-getsockname) o [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) possono restituire un indirizzo IPv6 mappato a IPv4 quando vengono usate in un socket dual stack. Se l'indirizzo IPv6 mappato a IPv4 restituito viene successivamente usato in un socket diverso che non è stato impostato su dual stack (un socket solo IPv6 che rappresenta il comportamento predefinito quando viene creato un socket), qualsiasi uso di questo socket solo IPv6 con un indirizzo IPv6 mappato a IPv4 avrà esito negativo. Il formato di indirizzo IPv6 mappato a IPv4 può essere usato solo in un socket a doppio stack.

In un socket di datagramma dual stack, se un'applicazione richiede la funzione [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) per restituire informazioni sui pacchetti in una struttura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) per i datagrammi ricevuti tramite IPv4, l'opzione del socket [IP \_ PKTINFO](ip-pktinfo.md) deve essere impostata su true nel socket. Se solo l'opzione [ \_ IPV6 PKTINFO](ipv6-pktinfo.md) è impostata su true nel socket, verranno fornite informazioni sui pacchetti per i datagrammi ricevuti tramite IPv6, ma potrebbero non essere disponibili per i datagrammi ricevuti tramite IPv4.

Se un'applicazione tenta di impostare l'opzione socket [IP \_ PKTINFO](ip-pktinfo.md) su un socket di datagramma a doppio stack e IPv4 è disabilitato nel sistema, la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) avrà esito negativo e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituirà un errore [WSAEINVAL](windows-sockets-error-codes-2.md). Questo stesso errore viene restituito anche dalla **funzione setsockopt** come risultato di altri errori. Se un'applicazione tenta di impostare un'opzione socket a livello IP IPPROTO in un socket a doppio stack e ha esito negativo con \_ [WSAEINVAL,](windows-sockets-error-codes-2.md)l'applicazione deve determinare se IPv4 è disabilitato nel computer locale. Un metodo che può essere usato per rilevare se IPv4 è abilitato o disabilitato è chiamare la funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) con il *parametro af* impostato su AF INET per provare a creare un \_ socket IPv4. Se la **funzione socket** ha esito negativo e **WSAGetLastError** restituisce un errore [WSAEAFNOSUPPORT,](windows-sockets-error-codes-2.md)significa che IPv4 non è abilitato. In questo caso, un errore della funzione **setsockopt** durante il tentativo di impostare l'opzione socket IP \_ PKTINFO può essere ignorato dall'applicazione. In caso contrario, un errore durante il tentativo di impostare \_ l'opzione socket IP PKTINFO deve essere considerato un errore imprevisto.

Per un socket dual stack quando si inviano datagrammi con la funzione [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) e un'applicazione vuole specificare un indirizzo IP locale specifico da usare, il metodo per gestire questo problema dipende dall'indirizzo IP di destinazione. Quando si esegue l'invio a un indirizzo di destinazione IPv4 o a un indirizzo di destinazione IPv6 mappato a IPv4, uno degli oggetti dati di controllo passati nella struttura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) a cui punta il *parametro lpMsg* deve contenere una struttura [**in \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) contenente l'indirizzo di origine IPv4 locale da usare per l'invio. Quando si invia a un indirizzo di destinazione IPv6 che non è un indirizzo IPv6 mappato a IPv4, uno degli oggetti dati di controllo passati nella struttura **WSAMSG** a cui punta il *parametro lpMsg* deve contenere una struttura [**\_ in6 pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) contenente l'indirizzo di origine IPv6 locale da usare per l'invio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida a IPv6 per Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Modifica delle strutture dei dati per le applicazioni Winsock IPv6](changing-data-structures-2.md)
</dt> <dt>

[Chiamate di funzione per applicazioni Winsock IPv6](function-calls-2.md)
</dt> <dt>

[Uso di indirizzi IPv4 hardcoded](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Interfaccia utente problemi relativi alle applicazioni Winsock IPv6](user-interface-issues-2.md)
</dt> <dt>

[Protocolli sottostanti per applicazioni Winsock IPv6](underlying-protocols-2.md)
</dt> <dt>

[**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername)
</dt> <dt>

[**getsockname**](/windows/desktop/api/winsock/nf-winsock-getsockname)
</dt> <dt>

[**in \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo)
</dt> <dt>

[**in6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo)
</dt> <dt>

[IP \_ PKTINFO](ip-pktinfo.md)
</dt> <dt>

[IPV6 \_ PKTINFO](ipv6-pktinfo.md)
</dt> <dt>

[**Setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> <dt>

[**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)
</dt> </dl>

 

 
