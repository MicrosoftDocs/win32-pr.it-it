---
title: Livelli ALE
description: Application Layer Enforcement (ALE) è costituito da diversi livelli di filtro e molti livelli di scarto corrispondenti.
ms.assetid: 3ac71787-2350-4a60-b0bf-b00b52d30b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a96e3b2ae5092bf8cca014eb3603eea5efe8f71
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336926"
---
# <a name="ale-layers"></a>Livelli ALE

L'applicazione a livello di applicazione (ALE) è costituita da diversi livelli di filtro e molti livelli di scarto corrispondenti. Tutti i livelli del motore di filtro della piattaforma filtro Windows (WFP), incluso ALE, sono descritti in [**filtro degli identificatori di livello**](management-filtering-layer-identifiers-.md). Questo argomento contiene una descrizione più dettagliata dei livelli di filtro che fanno parte di ALE.

## <a name="resource_assignment"></a>assegnazione di risorse \_

Per le operazioni di binding di rete, esplicito o implicito, viene associato un filtro a livello di [**\_ assegnazione di risorse FWPM livello \_ ale \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) .

Se viene confrontato un filtro a questo livello per autorizzare la creazione di socket non elaborati, il [**flag di condizione FWP è il flag \_ \_ \_ \_ \_ endpoint non elaborato**](filtering-condition-flags-.md) verrà impostato.

Se per un filtro a questo livello viene stabilita una corrispondenza per autorizzare la ricezione in modalità promiscua, il campo della [**modalità di FWP \_ condizione \_ ale \_ \_**](filtering-condition-identifiers-.md) viene impostato su sio \_ RCVALL. Per una descrizione di SIO \_ RCVALL, vedere [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl).

> [!Note]  
> Si tratta dell'unico livello in cui è possibile filtrare la modalità promiscua.

 

Se durante l'operazione **Bind ()** non viene specificata alcuna porta, ovvero se la porta è impostata su 0 (zero), lo stack TCP/IP selezionerà una porta dall'intervallo di porte dinamiche (19152 – 65535). La porta selezionata verrà classificata a questo livello insieme al [**flag di condizione FWP è il flag di \_ \_ \_ \_ \_ binding con caratteri jolly**](filtering-condition-flags-.md) .

Se l'indirizzo locale non è specificato nella chiamata [**Bind ()**](/windows/desktop/api/winsock/nf-winsock-bind) , il campo indirizzo locale è impostato su [**FWP \_ empty**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).

## <a name="auth_listen"></a>AUTENTICAZIONE in \_ ascolto

Un filtro a livello di [**FWPM \_ Layer \_ ale \_ auth \_ Listen \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) viene associato alle chiamate di [**ascolto TCP ()**](/windows/desktop/api/winsock2/nf-winsock2-listen) .

## <a name="auth_recv_accept"></a>\_accetta ricezione di autenticazione \_

Un filtro a livello di [**FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) viene abbinato per le chiamate TCP [**Accept ()**](/windows/desktop/api/winsock2/nf-winsock2-accept) , per i primi pacchetti UDP (unicast) da una tupla di porta/indirizzo remoto univoca e per i primi messaggi ICMP non di errore in ingresso (unicast) con un tipo, un codice e un ID ICMP univoco.

> [!Note]  
> I protocolli che non sono TCP o ICMP sono trattati come UDP.

 

I pacchetti TCP ricevuti dai socket non elaborati vengono gestiti in modo analogo al traffico UDP. Ovvero solo la prima [**trasmissione TCP ()**](/windows/desktop/api/winsock2/nf-winsock2-send) e il primo [**ricezione TCP ()**](/windows/desktop/api/winsock/nf-winsock-recv) su socket non elaborati verranno filtrati.

## <a name="auth_connect"></a>\_Connetti autenticazione

Un filtro a livello di [**FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) viene associato per le chiamate TCP [**()**](/windows/desktop/api/winsock2/nf-winsock2-connect) , per i primi pacchetti UDP inviati a un indirizzo remoto univoco e una tupla di porta e per i primi messaggi ICMP non di errore in uscita con un tipo, un codice e un ID ICMP univoco.

> [!Note]  
> I protocolli che non sono TCP o ICMP sono trattati come UDP.

 

I pacchetti TCP inviati da socket non elaborati vengono gestiti in modo analogo al traffico UDP. Ovvero solo la prima [**trasmissione TCP ()**](/windows/desktop/api/winsock2/nf-winsock2-send) e il primo [**ricezione TCP ()**](/windows/desktop/api/winsock/nf-winsock-recv) su socket non elaborati verranno filtrati.

## <a name="flow_established"></a>FLUSSO \_ stabilito

Al termine di un handshake TCP a tre vie, un filtro a livello di FWPM layer ale ha stabilito la corrispondenza del livello [**\_ \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) . Per il traffico non TCP, il filtro viene associato immediatamente dopo che sono state soddisfatte le corrispondenze dei filtri dei livelli di **autenticazione \_ ricezione \_ Accept** o **auth \_ Connect** .

Un filtro a questo livello non deve restituire un blocco o un permesso.

Questo livello viene usato dai driver di callout per tenere traccia dello stato della connessione, descritto in dettaglio nella documentazione di [Windows Driver Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) .

## <a name="resource_release"></a>versione della risorsa \_

Un filtro a livello [**di \_ FWPM \_ livello \_ ale \_ versione \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) viene abbinato dopo che sono state liberate le risorse allocate tramite l' **\_ assegnazione di risorse** .

## <a name="endpoint_closure"></a>\_chiusura endpoint

Viene stabilita una corrispondenza tra un filtro a livello di [**FWPM \_ Layer ale che chiude il livello \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) quando si chiude un flusso TCP connesso o un endpoint socket UDP.

## <a name="connect_redirect"></a>Connetti \_ Reindirizzamento

Un filtro a livello di [**FWPM \_ Layer \_ ale \_ Connect \_ Reindirizzamento \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) consente di modificare gli indirizzi e le porte remote. La connessione in uscita verrà reindirizzata per la durata di tale connessione.

## <a name="bind_redirect"></a>Reindirizzamento di binding \_

Un filtro a livello di [**FWPM \_ Layer \_ ale \_ Bind \_ Reindirizzamento \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) consente di modificare l'indirizzo locale e le porte del socket sottostante. Il socket locale verrà reindirizzato per la durata del socket

## <a name="ale-discard-layers"></a>Livelli di eliminazione ALE

Per ognuno dei livelli ALE descritti sopra, il motore di filtro contiene un livello di scarto corrispondente. I livelli di eliminazione delle ALE vengono usati dai callout a scopo di registrazione. I pacchetti e le indicazioni che sono stati eliminati in uno dei livelli di filtro ALE sono indicati al livello di eliminazione delle ALE corrispondente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Application Layer Enforcement (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Filtro con stato ALE](ale-stateful-filtering.md)
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
</dt> <dt>

[**Flag di condizione di filtro**](filtering-condition-flags-.md)
</dt> <dt>

[**Condizioni di filtro disponibili a ogni livello di filtro**](filtering-conditions-available-at-each-filtering-layer.md)
</dt> </dl>

 

 