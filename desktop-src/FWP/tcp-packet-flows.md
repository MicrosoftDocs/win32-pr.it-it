---
title: Flussi di pacchetti TCP
description: Ordine in cui i livelli del motore di filtro della piattaforma filtro Windows (WFP) vengono attraversati durante una tipica sessione TCP.
ms.assetid: 75319c91-f77b-4dec-b94f-36772f1f1d53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2203ccb4b2793983bd5b1052d53c2700d3033a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955641"
---
# <a name="tcp-packet-flows"></a>Flussi di pacchetti TCP

In questa sezione viene descritto l'ordine in cui i livelli del motore di filtro della piattaforma filtro Windows (WFP) vengono attraversati durante una tipica sessione TCP.

> [!Note]  
> I flussi di pacchetti TCP per IPv6 seguono lo stesso modello di IPv4.

 

> [!Note]  
> I flussi di pacchetti non TCP seguono lo stesso modello dei [flussi di pacchetti UDP](udp-packet-flows.md).

 

## <a name="tcp-connection-establishment"></a>Creazione connessione TCP

<dl> Il server (ricevitore) esegue l'apertura passiva

-   Binding: FWPM \_ Layer \_ ale \_ binding \_ Redirect \_ V4 (solo windows 7/Windows Server 2008 R2)
-   Binding: \_ assegnazione di risorse FWPM livello \_ ale \_ \_ \_ V4
-   ascolto: FWPM \_ Layer \_ ale \_ auth \_ Listen \_ V4

  
Il client (mittente) esegue l'apertura attiva

-   Binding: FWPM \_ Layer \_ ale \_ binding \_ Redirect \_ V4 (solo windows 7/Windows Server 2008 R2)
-   Binding: \_ assegnazione di risorse FWPM livello \_ ale \_ \_ \_ V4
-   Connetti: FWPM \_ Layer \_ ale \_ Connect \_ Redirect \_ V4 (solo windows 7/Windows Server 2008 R2)
-   connessione: FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V4
-   SYN: FWPM \_ livello di \_ trasporto in uscita \_ \_ V4
-   SYN: FWPM \_ Layer in \_ uscita \_ IPPACKET \_ V4

  
Server

-   SYN: FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V4
-   SYN: FWPM \_ livello di \_ trasporto in ingresso \_ \_ V4
-   SYN: FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V4
-   SYN-ACK: \_ trasporto in \_ uscita livello FWPM \_ \_ V4
-   SYN-ACK: FWPM \_ Layer in \_ uscita \_ IPPACKET \_ V4

  
Client

-   SYN-ACK: FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V4
-   SYN-ACK: FWPM \_ livello di \_ trasporto in ingresso \_ \_ V4
-   FWPM \_ Layer \_ ale \_ ha \_ stabilito \_ V4
-   ACK: \_ trasporto in \_ uscita livello FWPM \_ \_ V4
-   ACK: FWPM \_ Layer in \_ uscita \_ IPPACKET \_ V4

  
Server

-   ACK: FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V4
-   ACK: FWPM \_ Layer \_ trasporto in \_ ingresso \_ V4
-   FWPM \_ Layer \_ ale \_ ha \_ stabilito \_ V4
-   Ascolto completato. Il server può eseguire un'accettazione.

  
</dl>

## <a name="tcp-syn-received-with-no-one-listening-on-the-port-or-protocol"></a>TCP SYN ricevuto senza un ascolto sulla porta o sul protocollo

Server (ricevitore)

-   SYN: FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V4
-   SYN: FWPM \_ Layer \_ trasporto in \_ ingresso \_ V4 \_ Elimina
-   RST: \_ trasporto in uscita del livello FWPM \_ \_ \_ V4
-   RST: FWPM \_ Layer in \_ uscita \_ IPPACKET \_ V4

> [!Note]  
> Il protocollo SYN TCP senza endpoint è indicato al momento dell'eliminazione del trasporto con una condizione di errore specifica. Blocca questo pacchetto all'eliminazione del trasporto per evitare che lo stack invii l'evento corrispondente (RST). Per un esempio di filtro in modalità Stealth, vedere [Impedisci l'analisi delle porte](preventing-port-scanning.md).

 

## <a name="data-transmitted-over-a-tcp-connection"></a>Dati trasmessi tramite una connessione TCP

<dl> Client (mittente)

-   trasmissione
-   dati: \_ flusso di livello FWPM \_ \_ V4
-   Segmenti TCP: \_ trasporto in uscita del livello FWPM \_ \_ \_ V4
-   IP datagrammi: FWPM \_ Layer in \_ uscita \_ IPPACKET \_ V4

  
Server (ricevitore)

-   IP datagrammi: FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V4
-   Segmenti TCP: \_ trasporto in \_ ingresso FWPM layer \_ \_ V4
-   dati: \_ flusso di livello FWPM \_ \_ V4
-   I dati sono disponibili per la lettura.

  
</dl>

## <a name="successful-reauthorization-of-a-tcp-packet"></a>Ricreazione di un pacchetto TCP riuscita

Server (ricevitore)

-   IP datagrammi: FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V4
-   Segmento TCP: \_ trasporto in \_ ingresso FWPM layer \_ \_ V4
-   Segmento TCP: FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ Accept \_ V4
-   dati: \_ flusso di livello FWPM \_ \_ V4 (in ingresso)

## <a name="failed-reauthorization-of-a-tcp-packet"></a>Non è stato possibile riautorizzare un pacchetto TCP

Server (ricevitore)

-   IP datagrammi: FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V4
-   Segmento TCP: \_ trasporto in \_ ingresso FWPM layer \_ \_ V4
-   Segmento TCP: FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ Accept \_ V4
-   Segmento TCP: FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ Accept \_ V4 \_ scartate

## <a name="tcp-connection-termination"></a>Terminazione connessione TCP

La chiusura della connessione TCP non è indicata a nessun livello di Pam.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riautorizzazione ALE](ale-re-authorization.md)
</dt> <dt>

[**Filtraggio degli identificatori del livello**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




