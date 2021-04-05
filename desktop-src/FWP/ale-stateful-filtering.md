---
title: Filtro con stato ALE
description: I filtri installati a livello di applicazione a livello di applicazione (ALE) di Windows Filtering Platform (WFP) eseguono un filtro di rete con stato.
ms.assetid: d5a3fcad-d55e-4a07-af21-cb40e5e9a9ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30cc1b4a5830efd0fef6dc28c88db85cd9c88cca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046741"
---
# <a name="ale-stateful-filtering"></a>Filtro con stato ALE

I filtri installati a livello di applicazione a livello di applicazione (ALE) di Windows Filtering Platform (WFP) eseguono un filtro di rete con stato. Un *flusso ale* viene usato come base per il filtro con stato ale.

Un flusso ALE è un modo per classificare il traffico di rete mediante il raggruppamento in base a un indirizzo IP di origine, un indirizzo IP di destinazione, una porta di origine, una porta di destinazione e un protocollo. Un flusso ALE potrebbe essere generico, ovvero uno o più descrittori potrebbero corrispondere a tutti gli elementi (o caratteri jolly \* ). Ad esempio, un flusso UDP ALE generico viene descritto come indirizzo IP di origine = \* , indirizzo IP di destinazione = \* , porta di origine = \* , porta di destinazione = \* e protocollo = UDP.

Una volta autorizzata una connessione, le connessioni in ingresso sono autorizzate al livello [**FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ Accept \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) layer and Outbound Connections at the **FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}** Layer), viene creato un flusso ale, in modo tale che, a blocco di una modifica dei criteri, tutti i pacchetti, in ingresso e in uscita, che appartengono allo stesso Poiché la modifica di un criterio potrebbe richiedere il blocco delle connessioni precedentemente consentite, è necessario [riautorizzare](ale-re-authorization.md) i flussi ale quando si verifica una modifica dei criteri.

Il filtro con stato di ALE riduce drasticamente il numero di classificazioni necessarie classificando solo il primo pacchetto che appartiene a un flusso ALE. Per confronto, il filtro senza stato richiede la classificazione di ogni pacchetto che attraversa la rete.

Un flusso ALE ha una direzione associata, ovvero la direzione del primo pacchetto del flusso. In questo modo è possibile disporre di criteri più flessibili, permettendo connessioni avviate in ingresso per avere criteri diversi dalle connessioni avviate in uscita.

## <a name="tcp-ale-flow"></a>Flusso TCP ALE

Un flusso di ALE per il traffico TCP è identificato dalle cinque tuple di TCP/IP (indirizzo IP di origine, indirizzo IP di destinazione, porta di origine, porta di destinazione e protocollo).

Un flusso TCP ALE ha la stessa durata di un socket TCP connesso. Un socket TCP connesso può essere un socket creato con [**Connect ()**](/windows/desktop/api/winsock2/nf-winsock2-connect) o un socket creato in seguito a una chiamata [**Accept ()**](/windows/desktop/api/winsock2/nf-winsock2-accept) .

ALE mantiene una relazione uno-a-uno tra un flusso TCP ALE e un blocco di controllo TCP (TCB).

## <a name="udp-ale-flow"></a>Flusso UDP ALE

> [!Note]  
> I protocolli che non sono TCP o ICMP sono trattati come UDP.

 

Un flusso di ALE per il traffico UDP è identificato dalle cinque tuple di TCP/IP (indirizzo IP di origine, indirizzo IP di destinazione, porta di origine, porta di destinazione e protocollo).

Un flusso UDP ALE viene creato in base a un socket UDP e rappresenta il peer remoto con cui l'applicazione sta comunicando. Un peer remoto è identificato da una tupla (indirizzo IP di destinazione e porta di destinazione).

Esiste una relazione uno-a-molti tra un socket UDP e i peer remoti a cui comunica.

Quando il socket UDP locale viene chiuso, verranno eliminati tutti i flussi ALE associati.

In assenza di chiusure socket, i flussi di ALE unicast UDP hanno un timeout di inattività [configurabile](ale-flow-customization.md) che per impostazione predefinita è 60 secondi. Se non viene inviato o ricevuto alcun pacchetto all'interno di questa finestra, il flusso di ALE verrà eliminato. Questo timeout predefinito viene abbreviato progressivamente quando il numero di ALE fluisce a livello di sistema fino a una determinata soglia.

## <a name="icmp-ale-flow"></a>Flusso ICMP ALE

Un flusso di ALE per il traffico ICMP è identificato dalle sei Tuple (indirizzo IP di origine, indirizzo IP di destinazione, tipo ICMP, codice ICMP, protocollo e ID ICMP). L'ID ICMP fa parte del flusso di ALE solo per il traffico Echo/Reply ICMP.

In assenza di chiusure socket, i flussi di ALE unicast ICMP hanno un timeout di inattività [configurabile](ale-flow-customization.md) che per impostazione predefinita è 60 secondi. Se non viene inviato o ricevuto alcun pacchetto all'interno di questa finestra, il flusso di ALE verrà eliminato. Questo timeout predefinito viene abbreviato progressivamente quando il numero di ALE fluisce a livello di sistema fino a una determinata soglia.

Solo i messaggi non di errore ICMP sono indicati ai livelli ALE. I messaggi di errore ICMP possono essere controllati nei \_ livelli di errore ICMP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Application Layer Enforcement (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Livelli ALE](ale-layers.md)
</dt> <dt>

[Traffico di broadcast/multicast ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Riautorizzazione ALE](ale-re-authorization.md)
</dt> <dt>

[Personalizzazione del flusso di ALE](ale-flow-customization.md)
</dt> <dt>

[Flussi di pacchetti TCP](tcp-packet-flows.md)
</dt> <dt>

[Flussi di pacchetti UDP](udp-packet-flows.md)
</dt> <dt>

[Funzioni Winsock](/windows/desktop/WinSock/winsock-functions)
</dt> </dl>

 

 