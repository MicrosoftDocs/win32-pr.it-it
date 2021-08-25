---
title: Livelli ALE
description: Application Layer Enforcement (ALE) è costituito da diversi livelli di filtro e molti livelli di eliminazione corrispondenti.
ms.assetid: 3ac71787-2350-4a60-b0bf-b00b52d30b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c9d13c7b5493171caa7216e8f2991e0350b79dd46dca612f241c9446cafa39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901011"
---
# <a name="ale-layers"></a>Livelli ALE

L'applicazione del livello applicazione (ALE) è costituita da diversi livelli di filtro e molti livelli di eliminazione corrispondenti. Tutti i livelli Windows del motore di filtro della piattaforma di filtraggio (WFP), incluso ALE, sono descritti in [**Identificatori dei livelli di filtro**](management-filtering-layer-identifiers-.md). Questo argomento contiene una descrizione più dettagliata dei livelli di filtro che fanno parte di ALE.

## <a name="resource_assignment"></a>ASSEGNAZIONE \_ DI RISORSE

Un filtro al livello [**FWPM \_ LAYER \_ ALE \_ RESOURCE ASSIGNMENT \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) corrisponde per le operazioni di associazione di rete, esplicite o implicite.

Se viene trovata una corrispondenza con un filtro a questo livello per autorizzare la creazione di socket non elaborati, verrà impostato il flag [**FWP \_ CONDITION FLAG IS RAW \_ \_ \_ \_ ENDPOINT.**](filtering-condition-flags-.md)

Se a questo livello viene trovata una corrispondenza per autorizzare la ricezione in modalità promiscua, il campo [**FWP \_ CONDITION \_ ALE \_ PROMISCUOUS \_ MODE**](filtering-condition-identifiers-.md) verrà impostato su SIO \_ RCVALL. Per una descrizione di SIO \_ RCVALL, vedere [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl).

> [!Note]  
> Questo è l'unico livello in cui è possibile filtrare la modalità promiscua.

 

Se durante **bind()** non viene specificata alcuna porta, ovvero la porta è impostata su 0 (zero), lo stack TCP/IP selezionerà una porta dall'intervallo di porte dinamico (19152-65535). La porta selezionata verrà classificata a questo livello insieme al [**flag FWP \_ CONDITION FLAG IS WILDCARD \_ \_ \_ \_ BIND.**](filtering-condition-flags-.md)

Se l'indirizzo locale non è specificato nella [**chiamata bind(),**](/windows/desktop/api/winsock/nf-winsock-bind) il campo dell'indirizzo locale viene impostato su [**FWP \_ EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).

## <a name="auth_listen"></a>AUTH \_ LISTEN

Un filtro al livello [**FWPM \_ LAYER \_ ALE \_ AUTH \_ LISTEN \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) corrisponde alle chiamate TCP [**listen().**](/windows/desktop/api/winsock2/nf-winsock2-listen)

## <a name="auth_recv_accept"></a>AUTH \_ RECV \_ ACCEPT

Un filtro al livello [**FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) corrisponde per le chiamate TCP [**accept(),**](/windows/desktop/api/winsock2/nf-winsock2-accept) per i primi pacchetti UDP (unicast) da una tupla di indirizzo/porta remota univoca e per i primi messaggi ICMP non di errore (unicast) in ingresso con un tipo, codice e ID ICMP univoci.

> [!Note]  
> I protocolli che non sono TCP o ICMP vengono trattati come UDP.

 

I pacchetti TCP ricevuti dai socket non elaborati vengono gestiti in modo analogo al traffico UDP. In altri modo, verranno filtrati solo il primo tcp [**send()**](/windows/desktop/api/winsock2/nf-winsock2-send) e il primo [**tcp recv()**](/windows/desktop/api/winsock/nf-winsock-recv) su socket non elaborati.

## <a name="auth_connect"></a>CONNESSIONE DI \_ AUTENTICAZIONE

Un filtro al livello [**FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) corrisponde per le chiamate TCP [**connect(),**](/windows/desktop/api/winsock2/nf-winsock2-connect) per i primi pacchetti UDP inviati a un indirizzo remoto univoco e a una tupla di porta e per i primi messaggi ICMP non di errore in uscita con un tipo, un codice e un ID ICMP univoci.

> [!Note]  
> I protocolli che non sono TCP o ICMP vengono trattati come UDP.

 

I pacchetti TCP inviati dai socket non elaborati vengono gestiti in modo analogo al traffico UDP. In altri modo, verranno filtrati solo il primo tcp [**send()**](/windows/desktop/api/winsock2/nf-winsock2-send) e il primo [**tcp recv()**](/windows/desktop/api/winsock/nf-winsock-recv) su socket non elaborati.

## <a name="flow_established"></a>FLUSSO \_ STABILITO

Un filtro al livello [**FWPM \_ LAYER \_ ALE \_ FLOW ESTABLISHED \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) viene abbinato dopo il completamento di un handshake a tre way TCP. Per il traffico non TCP, il filtro viene abbinato immediatamente dopo la corrispondenza dei filtri dai livelli **AUTH \_ RECV \_ ACCEPT** o **AUTH \_ CONNECT.**

Un filtro a questo livello non deve restituire Block o Permit.

Questo livello viene usato dai driver callout per tenere traccia dello stato di connessione, descritto in dettaglio nella documentazione di [Windows Driver Kit.](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)

## <a name="resource_release"></a>VERSIONE \_ DELLE RISORSE

Un filtro al livello [**FWPM \_ LAYER \_ ALE \_ RESOURCE RELEASE \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) corrisponde dopo che le risorse allocate tramite **RESOURCE \_ ASSIGNMENT** sono state liberate.

## <a name="endpoint_closure"></a>CHIUSURA \_ DELL'ENDPOINT

Un filtro al livello [**FWPM \_ LAYER \_ ALE \_ ENDPOINT CLOSURE \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) viene abbinato quando viene chiuso un flusso TCP connesso o un endpoint socket UDP.

## <a name="connect_redirect"></a>REINDIRIZZAMENTO \_ CONNECT

Un filtro al livello [**FWPM \_ LAYER \_ ALE \_ CONNECT REDIRECT \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) consente la modifica di indirizzi e porte remoti. La connessione in uscita verrà reindirizzata per la durata della connessione.

## <a name="bind_redirect"></a>REINDIRIZZAMENTO \_ BIND

Un filtro al livello [**FWPM \_ LAYER \_ ALE \_ BIND REDIRECT \_ \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) consente di modificare l'indirizzo locale e le porte del socket sottostante. Il socket locale verrà reindirizzato per la durata del socket

## <a name="ale-discard-layers"></a>Livelli DISCARD di ALE

Per ogni livello ALE descritto in precedenza, il motore di filtro contiene un livello di eliminazione corrispondente. I livelli di eliminazione ale vengono usati dai callout a scopo di registrazione. I pacchetti e le indicazioni che sono stati eliminati in uno dei livelli di filtro ALE vengono indicati al livello di eliminazione ALE corrispondente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazione a livello di applicazione (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Filtro con stato ALE](ale-stateful-filtering.md)
</dt> <dt>

[Traffico multicast/broadcast ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Riautorizzazione ALE](ale-re-authorization.md)
</dt> <dt>

[Personalizzazione Flow ale](ale-flow-customization.md)
</dt> <dt>

[Flussi di pacchetti TCP](tcp-packet-flows.md)
</dt> <dt>

[Flussi di pacchetti UDP](udp-packet-flows.md)
</dt> <dt>

[Funzioni di Winsock](/windows/desktop/WinSock/winsock-functions)
</dt> <dt>

[**Flag di condizione di filtro**](filtering-condition-flags-.md)
</dt> <dt>

[**Condizioni di filtro disponibili a ogni livello di filtro**](filtering-conditions-available-at-each-filtering-layer.md)
</dt> </dl>

 

 