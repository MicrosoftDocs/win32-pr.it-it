---
description: "WS-Discovery definisce l'indirizzamento logico usando gli URI basati sul formato urn: UUID:."
ms.assetid: ed152f53-2996-4b90-8c4a-d187af0a598b
title: Uso di indirizzi logici e fisici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e11ddf1dc6fe34325a90f52e43346e507d837ab3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306863"
---
# <a name="using-logical-and-physical-addresses"></a>Uso di indirizzi logici e fisici

[WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) definisce l'indirizzamento logico mediante gli URI in base al `urn:uuid:` formato. Lo scopo di questo schema di indirizzamento è differenziare l'identità del dispositivo dal relativo indirizzo IP corrente. Questo schema fornisce essenzialmente la funzionalità dei nomi DNS senza richiedere un server dei nomi. [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) suggerisce che i dispositivi usino questo schema di indirizzamento.

DPWS consiglia inoltre ai servizi di utilizzare indirizzi fisici (detti anche trasporto). Questo consente ai client che non supportano in modo nativo WS-Discovery meccanismi di indirizzamento per comunicare con i servizi DPWS. Ogni servizio può inoltre definire i relativi indirizzi, che consente l'indirizzamento a livello di trasporto per le implementazioni dei dispositivi che gestiscono l'invio di servizi a un livello inferiore. Infine, l'utilizzo di indirizzi fisici ottimizza l'interoperabilità.

Lo svantaggio dell'indirizzamento fisico è che aggiunge complessità alle implementazioni dei dispositivi, in quanto l'indirizzo IP o di trasporto corrente deve essere rilevato e i metadati del dispositivo devono essere modificati di conseguenza. Per questo motivo, DPWS non richiede l'utilizzo di indirizzi di trasporto da servizi.

Se si usano indirizzi logici, esistono alcuni scenari in cui il comportamento di implementazione non è definito. La specifica WS-Discovery non descrive il significato di un servizio che si trova in un indirizzo logico. R1001 della specifica WS-Discovery consiglia di non usare WS-Discovery sui servizi ospitati a causa del chiacchiericcio di rete associato.

Non è consigliabile che i servizi si trovino in indirizzi logici in quanto questo riduce l'interoperabilità. Se un'implementazione deve trovarsi in un indirizzo logico, il servizio deve usare lo stesso indirizzo logico del dispositivo. Se questa operazione aggiunge una complessità eccessiva al modello di invio sul dispositivo, la soluzione consigliata consiste nell'usare i parametri di riferimento per distinguere i servizi. WSDAPI invierà correttamente messaggi ai servizi se utilizzano lo stesso indirizzo endpoint del dispositivo.

 

 



