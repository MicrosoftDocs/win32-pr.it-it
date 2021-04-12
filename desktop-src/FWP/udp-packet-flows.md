---
title: Flussi di pacchetti UDP
description: Ordine in cui i livelli del motore di filtro della piattaforma filtro Windows (WFP) vengono attraversati durante una tipica sessione UDP.
ms.assetid: ab618c1f-3e7c-4f4b-b4ff-9e396d3258d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 790de49e971d5506c1732b9c4d30b88643c7af0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331308"
---
# <a name="udp-packet-flows"></a>Flussi di pacchetti UDP

In questa sezione viene descritto l'ordine in cui i livelli del motore di filtro della piattaforma filtro Windows (WFP) vengono attraversati durante una tipica sessione UDP.

> [!Note]  
> I flussi di pacchetti UDP per IPv6 seguono lo stesso modello di IPv4.

 

> [!Note]  
> Tutti i flussi di pacchetti non TCP seguono lo stesso modello dei flussi di pacchetti UDP.

 

## <a name="udp-connection-establishment"></a>Creazione connessione UDP

<dl> Il server (ricevitore) esegue l'apertura passiva

-   Binding: FWPM \_ Layer \_ ale \_ binding \_ Redirect \_ V4 (solo windows 7/Windows Server 2008 R2)
-   Binding: \_ assegnazione di risorse FWPM livello \_ ale \_ \_ \_ V4

  
Il client (mittente) esegue l'apertura attiva

-   Binding: FWPM \_ Layer \_ ale \_ binding \_ Redirect \_ V4 (solo windows 7/Windows Server 2008 R2)
-   Binding: \_ assegnazione di risorse FWPM livello \_ ale \_ \_ \_ V4
-   SendTo: FWPM \_ Layer \_ ale \_ Connect \_ Reindirizzamento \_ V4 (solo windows 7/Windows Server 2008 R2)
-   SendTo: FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V4
-   FWPM \_ Layer \_ ale \_ ha \_ stabilito \_ V4
-   dati: \_ \_ dati datagramma FWPM layer \_ \_ V4
-   Messaggio UDP: \_ trasporto in uscita del livello FWPM \_ \_ \_ V4
-   IP datagrammi: FWPM \_ Layer in \_ uscita \_ IPPACKET \_ V4

  
Server

-   IP datagrammi: FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V4
-   Messaggio UDP: \_ trasporto in \_ ingresso FWPM layer \_ \_ V4
-   Messaggio UDP: FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ Accept \_ V4
-   FWPM \_ Layer \_ ale \_ ha \_ stabilito \_ V4
-   dati: \_ \_ dati datagramma FWPM layer \_ \_ V4

  
</dl>

## <a name="udp-message-received-with-no-one-listening-on-the-port-or-protocol"></a>Messaggio UDP ricevuto senza un ascolto sulla porta o sul protocollo

Server (ricevitore)

-   IP datagrammi: FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V4
-   IP datagrammi: FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V4 \_
-   Destinazione ICMP non raggiungibile: \_ \_ errore ICMP in uscita livello \_ FWPM \_ \_ V4
-   Destinazione ICMP non raggiungibile: FWPM \_ livello di \_ trasporto in \_ uscita \_ V4
-   Destinazione ICMP non raggiungibile: livello FWPM \_ in \_ uscita \_ IPPACKET \_ V4

> [!Note]  
> UDP senza endpoint è indicato in IPPACKET scarti con una condizione di errore specifica. Blocca questo pacchetto in IPPACKET scarta per evitare che lo stack invii l'evento corrispondente (errore ICMP).

 

## <a name="successful-reauthorization-of-a-udp-packet"></a>La riautorizzazione di un pacchetto UDP è stata completata

Server (ricevitore)

-   IP datagrammi: FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V4
-   Messaggio UDP: \_ trasporto in \_ ingresso FWPM layer \_ \_ V4
-   Messaggio UDP: FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ Accept \_ V4
-   Messaggio UDP: \_ \_ dati datagramma FWPM livello \_ \_ V4 (in ingresso)

## <a name="failed-reauthorization-of-a-udp-packet"></a>Non è stato possibile riautorizzare un pacchetto UDP

Server (ricevitore)

-   IP datagrammi: FWPM \_ Layer in \_ ingresso \_ IPPACKET \_ V4
-   Messaggio UDP: \_ trasporto in \_ ingresso FWPM layer \_ \_ V4
-   Messaggio UDP: FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ Accept \_ V4
-   Messaggio UDP: FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ Accept \_ V4 \_ scartate

## <a name="udp-connection-termination"></a>Terminazione connessione UDP

La chiusura della connessione UDP non è indicata a nessun livello di Pam.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riautorizzazione ALE](ale-re-authorization.md)
</dt> <dt>

[**Filtraggio degli identificatori del livello**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




