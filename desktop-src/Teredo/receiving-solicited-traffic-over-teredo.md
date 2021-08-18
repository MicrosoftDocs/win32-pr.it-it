---
title: Ricezione di traffico richiesto su Teredo
description: Molte applicazioni, ad esempio Microsoft Internet Explorer e Microsoft Outlook solo avviare connessioni a Internet.
ms.assetid: bff5d65e-050d-4b09-9982-8024612ffa6e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f003755f49d04113108f83c8d3eff67084364ad6dfcf8e9f40cf1bf7e142e0a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001679"
---
# <a name="receiving-solicited-traffic-over-teredo"></a>Ricezione di traffico richiesto su Teredo

Molte applicazioni, ad esempio Microsoft Internet Explorer e Microsoft Outlook solo avviare connessioni a Internet. Per queste applicazioni, [Teredo](about-teredo.md) connettività senza problemi su IPv6 in assenza di altre interfacce IPv6. Inoltre, il traffico richiesto può essere ricevuto tramite l'interfaccia Teredo nelle piattaforme precedenti di Microsoft Windows XP con Service Pack 2 (SP2) e Windows Server 2003.

La documentazione seguente illustra in che modo queste applicazioni possono ottenere la connettività e le circostanze in cui Teredo viene usato.

## <a name="obtaining-a-destination-address"></a>Recupero di un indirizzo di destinazione

Un'applicazione tenta di ottenere l'indirizzo di destinazione usando vari metodi, ad esempio Domain Name System (DNS) o Peer Name Resolution Protocol (PNRP). L'applicazione può ottenere più indirizzi IP IPv4 e IPv6 usando questi metodi. Le API tipiche usate per ottenere gli indirizzi IP includono l'API Windows XP [**GetHostByName**](/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname) e la nuova API Windows Vista [**GetAddrInfo.**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) Ad esempio, l'uso dell'API GetAddrInfo con il parametro della famiglia di intelligenza artificiale impostato su AF INET6 come hint addrinfo/protocol consente all'utente di eseguire query specifiche sui server DNS per gli indirizzi *\_* \_ IPv6. [**L'API DnsQuery**](/windows/desktop/api/windns/nf-windns-dnsquery_a) con tipo DNS TYPE AAAA può essere usata anche per eseguire query sui server \_ DNS per i record \_ AAAA.

## <a name="establishing-a-connection"></a>Istituzione di una connessione

Una connessione stabilita con Teredo viene descritta come "facile" perché viene gestita come qualsiasi altra connessione IPv6. La programmazione di un'applicazione non richiede considerazioni speciali per poter usare l'Teredo predefinita. Quando viene stabilita una connessione tra Teredo, non è necessario un router di inoltro, tipico di 6to4 e altre interfacce native. Tuttavia, Teredo è progettata come tecnologia di transizione di ultima risorsa per la connettività IPv6.

> [!Note]  
> Teredo non viene utilizzato se il nome host fornito viene risolto solo in indirizzi IPv4.

 

Quando un'applicazione tenta di connettersi a una destinazione usando indirizzi IPv6, si verifica quanto segue:

-   L'applicazione ottiene un elenco di indirizzi IPv6 chiamando l'API [**GetAdaptersAddresses.**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) Lo stack Windows Vista restituisce un elenco di tutte le interfacce in base all'ordinamento specificato in [RFC 3484.](https://www.irt.org/rfc/rfc3484.htm) Di conseguenza, le interfacce IPv6 e 6to4 IPv6 verranno elencate prima dell'Teredo interfaccia. Tuttavia, quando la connettività nativa IPv6 o 6to4 non è disponibile, Teredo sarà l'unica interfaccia che supporta IPv6 elencata.

    È importante ricordare che un'applicazione può usare qualsiasi interfaccia fornita dallo stack di Windows Vista, tuttavia l'ordinamento dell'elenco di interfacce restituito nella maggior parte dei casi comporterà l'Teredo dell'ultimo tentativo.

-   Prima Windows Vista tenta una connessione sull'interfaccia Teredo, il sistema operativo garantisce che l'indirizzo IPv6 si sia stabilizzato. Questa operazione viene eseguita automaticamente per le connessioni in uscita e non è una considerazione fondamentale per un'applicazione. Nel caso in cui l'applicazione sia necessaria per garantire la stabilità degli indirizzi, è possibile chiamare l'API [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable) per assicurarsi che l'indirizzo Teredo sia stabile.

-   Un Teredo inter interface tenterà di connettersi a un'altra Teredo nella destinazione. Se non Teredo'interfaccia utente, viene stabilita una connessione con un indirizzo di destinazione nativo o 6to4 tramite un inoltro specifico dell'host.

È anche possibile che le applicazioni che avviano connessioni a Internet ricevano traffico non richiesto. Per altri dettagli, [vedere Ricezione di traffico non](receiving-unsolicited-traffic-over-teredo.md)richiesto Teredo .

## <a name="using-the-wsaconnectbyname-api"></a>Uso dell'API WSAConnectByName

Chiamando l'API WSAConnectByName, è possibile che un'applicazione si connetta a un nome di destinazione anziché specificare l'indirizzo IP esatto. Lo stack Windows Vista preferisce IPv6 rispetto a IPv4 e, di conseguenza, tutti i tentativi di connessione verranno effettuati prima agli indirizzi IPv6.

La chiamata all'API WSAConnectByName ordinerà tutti gli indirizzi IP di destinazione ottenuti nell'ordine seguente:

-   Indirizzo IPv6 nativo
-   Indirizzo IP 6to4
-   IPv4 address (Indirizzo IPv4)
-   Teredo indirizzo

Dopo che gli indirizzi di destinazione sono stati ordinati internamente, viene tentata una connessione alla destinazione in base alla route migliore disponibile nell'host locale per l'indirizzo di destinazione. Come indicato dall'ordine degli indirizzi ordinati, se il nome di destinazione viene risolto in un indirizzo IPv4 e Teredo, l'indirizzo IPv4 verrà usato per stabilire la connessione.

L'API WSAConnectByName funziona internamente per trovare la corrispondenza migliore tra gli indirizzi. Questo tentativo si basa sulle route disponibili nell'host locale e sugli indirizzi di destinazione.

A causa dell'assenza corrente Teredo inoltri su Internet, è improbabile che le connessioni agli indirizzi IPv6 nativi riescano sull Teredo intervallo. Se viene chiamato WSAConnectByName, Windows Vista non emettere query AAAA quando Teredo è l'unica interfaccia che supporta IPv6 disponibile. In questo modo si garantisce che gli indirizzi IPv6 nativi non siano ottenuti come destinazione e che le connessioni vengono tentate tramite IPv4, che ha la massima probabilità di esito positivo. Per ottenere indirizzi IPv6 quando Teredo è l'unica interfaccia che supporta IPv6, un'applicazione deve usare in modo esplicito l'API DnsQuery per i record AAAA.

 

 