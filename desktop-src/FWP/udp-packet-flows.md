---
title: Flussi di pacchetti UDP
description: Ordine in cui i livelli del motore di filtro Windows Filtering Platform (WFP) vengono attraversati durante una sessione UDP tipica.
ms.assetid: ab618c1f-3e7c-4f4b-b4ff-9e396d3258d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9e850f67bce9a001d41ebb54b17d3d0d86b94b22f083529e4589d6b69841b7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746641"
---
# <a name="udp-packet-flows"></a>Flussi di pacchetti UDP

Questa sezione descrive l'ordine in cui i livelli del motore di filtro Windows Filtering Platform (WFP) vengono attraversati durante una tipica sessione UDP.

> [!Note]  
> I flussi di pacchetti UDP per IPv6 seguono lo stesso modello di IPv4.

 

> [!Note]  
> Tutti i flussi di pacchetti non TCP seguono lo stesso modello dei flussi di pacchetti UDP.

 

## <a name="udp-connection-establishment"></a>Stabilire una connessione UDP

<dl> Il server (ricevitore) esegue l'apertura passiva

-   bind: FWPM \_ LAYER \_ ALE \_ BIND REDIRECT \_ \_ V4 (solo Windows 7/Windows Server 2008 R2)
-   bind: FWPM \_ LAYER \_ ALE \_ RESOURCE ASSIGNMENT \_ \_ V4

  
Il client (mittente) esegue l'apertura attiva

-   bind: FWPM \_ LAYER \_ ALE \_ BIND REDIRECT \_ \_ V4 (solo Windows 7/Windows Server 2008 R2)
-   bind: FWPM \_ LAYER \_ ALE \_ RESOURCE ASSIGNMENT \_ \_ V4
-   sendto: FWPM \_ LAYER \_ ALE \_ CONNECT REDIRECT \_ \_ V4 (solo Windows 7/Windows Server 2008 R2)
-   sendto: FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V4
-   FWPM \_ LAYER \_ ALE \_ FLOW \_ ESTABLISHED \_ V4
-   data: FWPM \_ LAYER \_ DATAGRAM \_ DATA \_ V4
-   Messaggio UDP: FWPM \_ LAYER \_ OUTBOUND TRANSPORT \_ \_ V4
-   Datagrammi IP: FWPM \_ LAYER \_ OUTBOUND \_ IPPACKET \_ V4

  
Server

-   Datagrammi IP: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4
-   Messaggio UDP: FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V4
-   Messaggio UDP: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4
-   FWPM \_ LAYER \_ ALE \_ FLOW \_ ESTABLISHED \_ V4
-   data: FWPM \_ LAYER \_ DATAGRAM \_ DATA \_ V4

  
</dl>

## <a name="udp-message-received-with-no-one-listening-on-the-port-or-protocol"></a>Messaggio UDP ricevuto senza nessuno in ascolto sulla porta o sul protocollo

Server (ricevitore)

-   Datagrammi IP: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4
-   Datagrammi IP: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4 \_ DISCARD
-   ICMP Dest Unreachable: FWPM \_ LAYER \_ OUTBOUND \_ ICMP \_ ERROR \_ V4
-   ICMP Dest Unreachable: FWPM \_ LAYER \_ OUTBOUND \_ TRANSPORT \_ V4
-   ICMP Dest Unreachable: FWPM \_ LAYER \_ OUTBOUND \_ IPPACKET \_ V4

> [!Note]  
> UDP senza endpoint viene indicato in IPPACKET discard con una condizione di errore specifica. Blocca questo pacchetto in IPPACKET discard per impedire allo stack di inviare l'evento corrispondente (errore ICMP).

 

## <a name="successful-reauthorization-of-a-udp-packet"></a>Riautorizzazione riuscita di un pacchetto UDP

Server (ricevitore)

-   Datagrammi IP: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4
-   Messaggio UDP: FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V4
-   Messaggio UDP: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4
-   Messaggio UDP: FWPM \_ LAYER \_ DATAGRAM \_ DATA \_ V4(INBOUND)

## <a name="failed-reauthorization-of-a-udp-packet"></a>Riautorizzazione non riuscita di un pacchetto UDP

Server (ricevitore)

-   Datagrammi IP: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4
-   Messaggio UDP: FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V4
-   Messaggio UDP: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4
-   Messaggio UDP: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4 \_ DISCARD

## <a name="udp-connection-termination"></a>Terminazione della connessione UDP

La terminazione della connessione UDP non è indicata a livello WFP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riautorizzazione ALE](ale-re-authorization.md)
</dt> <dt>

[**Filtro degli identificatori di livello**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




