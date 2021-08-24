---
title: Flussi di pacchetti TCP
description: L'ordine in cui i livelli del motore di filtro Windows Filtering Platform (WFP) vengono attraversati durante una tipica sessione TCP.
ms.assetid: 75319c91-f77b-4dec-b94f-36772f1f1d53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47d4836da7a1912a6e39358b54e2a3086dd80efe844d6a301d079014d4a5b209
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746631"
---
# <a name="tcp-packet-flows"></a>Flussi di pacchetti TCP

Questa sezione descrive l'ordine in cui i livelli del motore di filtro Windows Filtering Platform (WFP) vengono attraversati durante una tipica sessione TCP.

> [!Note]  
> I flussi di pacchetti TCP per IPv6 seguono lo stesso modello di IPv4.

 

> [!Note]  
> I flussi di pacchetti non TCP seguono lo stesso modello dei [flussi di pacchetti UDP.](udp-packet-flows.md)

 

## <a name="tcp-connection-establishment"></a>Stabilire una connessione TCP

<dl> Il server (ricevitore) esegue l'apertura passiva

-   bind: FWPM \_ LAYER \_ ALE \_ BIND REDIRECT \_ \_ V4 (solo Windows 7/Windows Server 2008 R2)
-   bind: FWPM \_ LAYER \_ ALE \_ RESOURCE ASSIGNMENT \_ \_ V4
-   listen: FWPM \_ LAYER \_ ALE \_ AUTH \_ LISTEN \_ V4

  
Il client (mittente) esegue l'apertura attiva

-   bind: FWPM \_ LAYER \_ ALE \_ BIND REDIRECT \_ \_ V4 (solo Windows 7/Windows Server 2008 R2)
-   bind: FWPM \_ LAYER \_ ALE \_ RESOURCE ASSIGNMENT \_ \_ V4
-   connect: FWPM \_ LAYER \_ ALE \_ CONNECT REDIRECT \_ \_ V4 (solo Windows 7/Windows Server 2008 R2)
-   connect: FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V4
-   SYN: FWPM \_ LAYER \_ OUTBOUND \_ TRANSPORT \_ V4
-   SYN: FWPM \_ LAYER \_ OUTBOUND \_ IPPACKET \_ V4

  
Server

-   SYN: LIVELLO FWPM \_ \_ IN INGRESSO \_ IPPACKET \_ V4
-   SYN: FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V4
-   SYN: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4
-   SYN-ACK: FWPM \_ LAYER \_ OUTBOUND \_ TRANSPORT \_ V4
-   SYN-ACK: \_ \_ IPPACKET \_ V4 IN USCITA DEL LIVELLO FWPM \_

  
Client

-   SYN-ACK: LIVELLO FWPM \_ \_ IN INGRESSO \_ IPPACKET \_ V4
-   SYN-ACK: FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V4
-   FWPM \_ LAYER \_ ALE \_ FLOW \_ ESTABLISHED \_ V4
-   ACK: FWPM \_ LAYER \_ OUTBOUND \_ TRANSPORT \_ V4
-   ACK: FWPM \_ LAYER \_ OUTBOUND \_ IPPACKET \_ V4

  
Server

-   ACK: FWPM \_ LAYER \_ INBOUND \_ IPPACKET \_ V4
-   ACK: FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V4
-   FWPM \_ LAYER \_ ALE \_ FLOW \_ ESTABLISHED \_ V4
-   L'ascolto è stato completato. Il server può eseguire un'accettazione.

  
</dl>

## <a name="tcp-syn-received-with-no-one-listening-on-the-port-or-protocol"></a>TCP SYN ricevuto senza nessuno in ascolto sulla porta o sul protocollo

Server (ricevitore)

-   SYN: LIVELLO FWPM \_ \_ IN INGRESSO \_ IPPACKET \_ V4
-   SYN: FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V4 \_ DISCARD
-   RST: FWPM \_ LAYER \_ OUTBOUND \_ TRANSPORT \_ V4
-   RST: \_ \_ IPPACKET \_ V4 IN USCITA DEL LIVELLO FWPM \_

> [!Note]  
> TCP SYN senza endpoint è indicato in TRANSPORT discard con una condizione di errore specifica. Blocca questo pacchetto in transport discard per fare in modo che lo stack non invii l'evento corrispondente (RST). Per un esempio di filtro in modalità mascheramento, vedere [Prevenzione dell'analisi delle porte.](preventing-port-scanning.md)

 

## <a name="data-transmitted-over-a-tcp-connection"></a>Dati trasmessi tramite una connessione TCP

<dl> Client (mittente)

-   trasmissione
-   data: FWPM \_ LAYER \_ STREAM \_ V4
-   Segmenti TCP: FWPM \_ LAYER \_ OUTBOUND TRANSPORT \_ \_ V4
-   Datagrammi IP: FWPM \_ LAYER \_ OUTBOUND \_ IPPACKET \_ V4

  
Server (ricevitore)

-   Datagrammi IP: LIVELLO FWPM \_ \_ IN INGRESSO \_ IPPACKET \_ V4
-   Segmenti TCP: FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V4
-   data: FWPM \_ LAYER \_ STREAM \_ V4
-   I dati sono disponibili per la lettura.

  
</dl>

## <a name="successful-reauthorization-of-a-tcp-packet"></a>Riautorizzazione riuscita di un pacchetto TCP

Server (ricevitore)

-   Datagrammi IP: LIVELLO FWPM \_ \_ IN INGRESSO \_ IPPACKET \_ V4
-   Segmento TCP: FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V4
-   Segmento TCP: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4
-   data: FWPM \_ LAYER \_ STREAM \_ V4(INBOUND)

## <a name="failed-reauthorization-of-a-tcp-packet"></a>Riautorizzazione non riuscita di un pacchetto TCP

Server (ricevitore)

-   Datagrammi IP: LIVELLO FWPM \_ \_ IN INGRESSO \_ IPPACKET \_ V4
-   Segmento TCP: FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V4
-   Segmento TCP: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4
-   Segmento TCP: FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V4 \_ DISCARD

## <a name="tcp-connection-termination"></a>Terminazione della connessione TCP

La terminazione della connessione TCP non è indicata a nessun livello WFP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riautorizzazione ALE](ale-re-authorization.md)
</dt> <dt>

[**Filtro degli identificatori dei livelli**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




