---
description: Per supportare sia IPv4 che IPv6 in Windows XP con Service Pack 1 (SP1) e in Windows Server 2003, un'applicazione deve creare due socket, un socket da usare con IPv4 e un socket per l'uso con IPv6.
ms.assetid: 7ae49081-ffb5-4eee-b488-2541398e7acc
title: Socket Dual-Stack per applicazioni Winsock IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 943d8150586bcf14a905ab32dcacaea63b7d6982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306991"
---
# <a name="dual-stack-sockets-for-ipv6-winsock-applications"></a>Socket Dual-Stack per applicazioni Winsock IPv6

Per supportare sia IPv4 che IPv6 in Windows XP con Service Pack 1 (SP1) e in Windows Server 2003, un'applicazione deve creare due socket, un socket da usare con IPv4 e un socket per l'uso con IPv6. Questi due socket devono essere gestiti separatamente dall'applicazione.

Windows Vista e versioni successive offrono la possibilità di creare un singolo socket IPv6 che può gestire sia il traffico IPv6 che quello IPv4. Ad esempio, viene creato un socket di ascolto TCP per IPv6, inserito in modalità dual stack e associato alla porta 5001. Questo socket a doppio stack può accettare connessioni da client TCP IPv6 che si connettono alla porta 5001 e dai client TCP IPv4 che si connettono alla porta 5001. Questa funzionalità consente di semplificare notevolmente la progettazione delle applicazioni e riduce il sovraccarico delle risorse richiesto per l'invio di operazioni su due socket distinti.

## <a name="creating-a-dual-stack-socket"></a>Creazione di un socket Dual-Stack

Per impostazione predefinita, un socket IPv6 creato in Windows Vista e versioni successive opera solo sul protocollo IPv6. Per creare un socket IPv6 in un socket a doppio stack, è necessario chiamare la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) con l'opzione socket **\_ V6ONLY di IPv6** per impostare questo valore su zero prima che il socket venga associato a un indirizzo IP. Quando l' **opzione \_ V6ONLY socket IPv6** è impostata su zero, un socket creato per la famiglia di indirizzi **AF \_ INET6** può essere usato per inviare e ricevere pacchetti da e verso un indirizzo IPv6 o un indirizzo mappato IPv4.

## <a name="ip-addresses-with-a-dual-stack-socket"></a>Indirizzi IP con un socket Dual-Stack

I socket a doppio stack richiedono sempre indirizzi IPv6. La possibilità di interagire con un indirizzo IPv4 richiede l'utilizzo del formato di indirizzo IPv6 mappato a IPv4. Tutti gli indirizzi IPv4 devono essere rappresentati nel formato di indirizzo IPv6 mappato IPv4, che consente a un'applicazione solo IPv6 di comunicare con un nodo IPv4. Il formato di indirizzo IPv6 con mapping IPv4 consente di rappresentare l'indirizzo IPv4 di un nodo IPv4 come indirizzo IPv6. L'indirizzo IPv4 è codificato nei bit 32 di ordine inferiore dell'indirizzo IPv6 e i 96 bit di ordine superiore contengono il prefisso fisso 0:0: 0:0: 0: FFFF. Il formato di indirizzo IPv6 mappato a IPv4 è specificato nella RFC 4291. Per ulteriori informazioni, vedere [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291). La \_ macro IN6ADDR SETV4MAPPED in *MSTCPIP. h* può essere utilizzata per convertire un indirizzo IPv4 nel formato di indirizzo IPv6 con mapping IPv4 richiesto.

Se il protocollo sottostante è effettivamente IPv4, viene eseguito il mapping dell'indirizzo IPv4 in un formato di indirizzo IPv6 mappato a IPv4. Ovvero, il campo famiglia nella struttura [sockaddr](sockaddr-2.md) indica AF \_ INET6, ma un indirizzo IPv6 con mapping IPv4 è codificato nella struttura degli indirizzi IPv6. Per un socket a doppio stack in modalità di ascolto, tutte le connessioni IPv4 accettate restituiranno un indirizzo IPv6 mappato IPv4. Per un socket a doppio stack che si connette a una destinazione IPv4, la struttura SOCKADDR passata a Connect deve essere un indirizzo IPv6 mappato a IPv4. È necessario che le applicazioni gestiscano questi indirizzi IPv6 con mapping IPv4 in modo appropriato e li usino solo con dual stack Sockets. Se un indirizzo IP deve essere passato a un socket IPv4 normale, l'indirizzo deve essere un indirizzo IPv4 normale, non un indirizzo IPv6 con mapping IPv4.

## <a name="potential-issues-using-a-dual-stack-socket"></a>Problemi potenziali usando un socket di Dual-Stack

Un potenziale problema per le applicazioni è ottenere un indirizzo IPv6 con mapping IPv4 in un socket a doppio stack e quindi provare a usare l'indirizzo IP restituito in un socket IPv6 diverso. Le funzioni [**getsockname**](/windows/desktop/api/winsock/nf-winsock-getsockname) o [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) , ad esempio, possono restituire un indirizzo IPv6 con mapping IPv4 quando viene usato in un socket a doppio stack. Se l'indirizzo IPv6 con mapping IPv4 restituito viene successivamente usato in un socket diverso che non è stato impostato su doppio stack (un socket IPv6 solo che è il comportamento predefinito quando viene creato un socket), qualsiasi uso di questo socket IPv6 solo con un indirizzo IPv6 con mapping IPv4 avrà esito negativo. Il formato di indirizzo IPv6 mappato a IPv4 può essere utilizzato solo in un socket a doppio stack.

In un socket di datagramma a doppio stack, se un'applicazione richiede che la funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) restituisca informazioni sui pacchetti in una struttura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) per datagrammi ricevuti su IPv4, l'opzione socket [IP \_ pktinfo](ip-pktinfo.md) deve essere impostata su true nel socket. Se solo l' [opzione \_ pktinfo IPv6](ipv6-pktinfo.md) è impostata su true nel socket, le informazioni sui pacchetti verranno fornite per i datagrammi ricevuti su IPv6, ma potrebbero non essere fornite per datagrammi ricevuti tramite IPv4.

Se un'applicazione prova a impostare l'opzione del socket [ \_ pktinfo IP](ip-pktinfo.md) su un socket di datagramma a doppio stack e IPv4 è disabilitato nel sistema, la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) avrà esito negativo e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituirà un errore di [WSAEINVAL](windows-sockets-error-codes-2.md). Questo stesso errore viene inoltre restituito dalla funzione **setsockopt** come risultato di altri errori. Se un'applicazione tenta di impostare un' \_ opzione socket a livello IP IPPROTO in un socket a doppio stack e non riesce con [WSAEINVAL](windows-sockets-error-codes-2.md), l'applicazione deve determinare se IPv4 è disabilitato nel computer locale. Un metodo che può essere usato per rilevare se IPv4 è abilitato o disabilitato consiste nel chiamare la funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) con il parametro *AF* impostato su AF \_ inet per provare a creare un socket IPv4. Se la funzione **socket** ha esito negativo e **WSAGetLastError** restituisce un errore di [WSAEAFNOSUPPORT](windows-sockets-error-codes-2.md), significa che IPv4 non è abilitato. In questo caso, un errore di funzione **setsockopt** durante il tentativo di impostare l' \_ opzione del socket IP pktinfo può essere ignorato dall'applicazione. In caso contrario, un errore durante il tentativo di impostare l' \_ opzione del socket pktinfo IP deve essere considerato un errore imprevisto.

Per un socket a doppio stack quando si inviano datagrammi con la funzione [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) e un'applicazione vuole specificare un indirizzo di origine IP locale specifico da usare, il metodo per gestirlo dipende dall'indirizzo IP di destinazione. Quando si invia a un indirizzo di destinazione IPv4 o a un indirizzo di destinazione IPv6 con mapping IPv4, uno degli oggetti dati del controllo passati nella struttura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) a cui fa riferimento il parametro *lpMsg* deve contenere una struttura [**\_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) che contiene l'indirizzo di origine IPv4 locale da utilizzare per l'invio. Quando si invia a un indirizzo di destinazione IPv6 che non è un indirizzo IPv6 con mapping IPv4, uno degli oggetti dati del controllo passati nella struttura **WSAMSG** a cui punta il parametro *lpMsg* deve contenere una struttura [**IN6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) che contiene l'indirizzo di origine IPv6 locale da usare per l'invio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida a IPv6 per le applicazioni Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Modifica delle strutture di dati per applicazioni Winsock IPv6](changing-data-structures-2.md)
</dt> <dt>

[Chiamate di funzione per applicazioni Winsock IPv6](function-calls-2.md)
</dt> <dt>

[Utilizzo di indirizzi IPv4 hardcoded](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Problemi dell'interfaccia utente per le applicazioni Winsock IPv6](user-interface-issues-2.md)
</dt> <dt>

[Protocolli sottostanti per applicazioni Winsock IPv6](underlying-protocols-2.md)
</dt> <dt>

[**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername)
</dt> <dt>

[**getsockname**](/windows/desktop/api/winsock/nf-winsock-getsockname)
</dt> <dt>

[**in \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo)
</dt> <dt>

[**\_pktinfo IN6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo)
</dt> <dt>

[\_pktinfo IP](ip-pktinfo.md)
</dt> <dt>

[\_Pktinfo IPv6](ipv6-pktinfo.md)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> <dt>

[**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)
</dt> </dl>

 

 
