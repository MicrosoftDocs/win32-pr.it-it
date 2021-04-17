---
title: Ricezione di traffico richiesto su Teredo
description: Molte applicazioni come Microsoft Internet Explorer e Microsoft Outlook avviano solo connessioni a Internet.
ms.assetid: bff5d65e-050d-4b09-9982-8024612ffa6e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035d067afeb9c62795efb5acd0bb28adc3afcb16
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104517176"
---
# <a name="receiving-solicited-traffic-over-teredo"></a>Ricezione di traffico richiesto su Teredo

Molte applicazioni come Microsoft Internet Explorer e Microsoft Outlook avviano solo connessioni a Internet. Per queste applicazioni, [Teredo](about-teredo.md) può garantire una connettività uniforme su IPv6 in assenza di altre interfacce IPv6. Inoltre, il traffico richiesto può essere ricevuto tramite l'interfaccia Teredo sulle piattaforme precedenti di Microsoft Windows XP con Service Pack 2 (SP2) e Windows Server 2003.

Nella documentazione seguente viene illustrato il modo in cui queste applicazioni raggiungono la connettività e le circostanze in cui viene utilizzato Teredo.

## <a name="obtaining-a-destination-address"></a>Acquisizione di un indirizzo di destinazione

Un'applicazione tenta di ottenere l'indirizzo di destinazione utilizzando diversi metodi, ad esempio Domain Name System (DNS) o il protocollo PNRP (Peer Name Resolution Protocol). È possibile che l'applicazione ottenga più indirizzi IP IPv4 e IPv6 usando questi metodi. Le API tipiche utilizzate per ottenere gli indirizzi IP includono l'API di Windows XP [**gethostbyname**](/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname) e la nuova API di Windows Vista [**funzione getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo). Ad esempio, l'uso dell'API funzione getaddrinfo con il parametro della *\_ famiglia ai* è impostato su AF \_ INET6 come hint per addrinfo/Protocol consente all'utente di eseguire query sui server DNS per indirizzi IPv6 in modo specifico. L'API [**DnsQuery**](/windows/desktop/api/windns/nf-windns-dnsquery_a) con tipo DNS \_ \_ aaaa può essere usata anche per eseguire query sui server DNS per i record AAAA.

## <a name="establishing-a-connection"></a>Istituzione di una connessione

Una connessione stabilita con Teredo viene descritta come ' seamless ' perché viene gestita come qualsiasi altra connessione IPv6. La programmazione di un'applicazione non richiede una particolare considerazione per poter utilizzare l'interfaccia Teredo. Quando viene stabilita una connessione tra le interfacce Teredo, non è necessario un router di inoltro, tipico di 6to4 e altre interfacce native. Tuttavia, Teredo è progettato come ultima tecnologia di transizione per la connettività IPv6.

> [!Note]  
> Teredo non viene utilizzato se il nome host fornito viene risolto solo negli indirizzi IPv4.

 

Quando un'applicazione tenta di connettersi a una destinazione usando indirizzi IPv6, si verificherà quanto segue:

-   L'applicazione ottiene un elenco di indirizzi IPv6 chiamando l'API [**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) . Lo stack di Windows Vista restituisce un elenco di tutte le interfacce basate sull'ordinamento specificato nella [RFC 3484](https://www.irt.org/rfc/rfc3484.htm). Di conseguenza, le interfacce IPv6 IPv6 e 6to4 verranno elencate prima dell'interfaccia Teredo. Tuttavia, quando non è disponibile la connettività IPv6 o 6to4 nativa, Teredo sarà l'unica interfaccia in grado di supportare IPv6 elencata.

    È importante ricordare che un'applicazione può utilizzare qualsiasi interfaccia fornita dallo stack di Windows Vista, tuttavia l'ordine dell'elenco di interfacce restituito genererà l'ultimo tentativo di Teredo.

-   Prima che Windows Vista tenti una connessione sull'interfaccia Teredo, il sistema operativo garantisce la stabilità dell'indirizzo IPv6. Questa operazione viene eseguita automaticamente per le connessioni in uscita e non è una considerazione cruciale per un'applicazione. Nel caso in cui l'applicazione sia necessaria per garantire la stabilità degli indirizzi, è possibile chiamare l'API [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable) per assicurarsi che l'indirizzo Teredo sia stabile.

-   Un'interfaccia Teredo tenterà di connettersi a un'altra interfaccia Teredo nella destinazione. Se non è presente un'interfaccia Teredo, viene stabilita una connessione con un indirizzo di destinazione nativo o 6to4 tramite un inoltro specifico dell'host.

È anche possibile che le applicazioni che avviano connessioni a Internet ricevano traffico non richiesto. Per altri dettagli, vedere [ricezione di traffico non richiesto su Teredo](receiving-unsolicited-traffic-over-teredo.md).

## <a name="using-the-wsaconnectbyname-api"></a>Uso dell'API con WSAConnectByName

Chiamando l'API con WSAConnectByName, è possibile che un'applicazione si connetta a un nome di destinazione invece di specificare l'indirizzo IP esatto. Lo stack di Windows Vista preferisce IPv6 su IPv4 e, di conseguenza, verranno prima eseguiti tutti i tentativi di connessione agli indirizzi IPv6.

Se si chiama l'API con WSAConnectByName, tutti gli indirizzi IP di destinazione ottenuti vengono ordinati nell'ordine seguente:

-   Indirizzo IPv6 nativo
-   Indirizzo IP 6to4
-   IPv4 address (Indirizzo IPv4)
-   Indirizzo Teredo

Quando gli indirizzi di destinazione vengono ordinati internamente, viene tentata una connessione alla destinazione in base alla route migliore disponibile nell'host locale per l'indirizzo di destinazione. Come indicato dall'ordine degli indirizzi ordinati, se il nome di destinazione viene risolto in un indirizzo IPv4 e Teredo, per stabilire la connessione verrà usato l'indirizzo IPv4.

L'API con WSAConnectByName funziona internamente per trovare la migliore corrispondenza tra gli indirizzi. Questo tentativo si basa sulle route disponibili nell'host locale e negli indirizzi di destinazione.

A causa dell'assenza corrente degli inoltri Teredo su Internet, è improbabile che le connessioni agli indirizzi IPv6 nativi siano riuscite sull'interfaccia Teredo. Se viene chiamato con WSAConnectByName, Windows Vista non emetterà query AAAA quando Teredo è l'unica interfaccia compatibile con IPv6 disponibile. In questo modo si garantisce che gli indirizzi IPv6 nativi non vengano ottenuti come destinazione e che le connessioni vengano tentate su IPv4, con la massima probabilità di successo. Per ottenere gli indirizzi IPv6 quando Teredo è l'unica interfaccia compatibile con IPv6, un'applicazione deve usare in modo esplicito l'API DnsQuery per i record AAAA.

 

 