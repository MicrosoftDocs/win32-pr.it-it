---
description: Il provider di servizi NLA (Network Location Awareness) è fondamentale per i computer o i dispositivi che potrebbero spostarsi tra reti diverse e per la selezione di configurazioni ottimali quando ne sono disponibili più di una.
ms.assetid: 307f384d-e59a-4fc5-8f6a-ed81a102df60
title: Ruolo di NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f44d517fc9f32d4fb61eb2b4d9b61c473bc946066e670fcb51f0ca2c753e692
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733341"
---
# <a name="the-role-of-nla"></a>Ruolo di NLA

Il provider di servizi NLA (Network Location Awareness) è fondamentale per i computer o i dispositivi che potrebbero spostarsi tra reti diverse e per la selezione di configurazioni ottimali quando ne sono disponibili più di una. Ad esempio, un computer wireless in roaming tra reti fisiche può usare NLA per determinare la configurazione appropriata in base alle informazioni sulla connessione di rete disponibile. L'interfaccia di rete si rivela utile anche quando un computer multihomed ha una connessione fisica a una rete, mentre è anche connessa a un'altra rete tramite una connessione remota o un tunnel.

In passato, gli sviluppatori dovevano ottenere informazioni su un'interfaccia di rete logica e quindi prendere decisioni sulla connettività di rete, in base a una vasta gamma di informazioni di rete diverse. In questi casi, gli sviluppatori dovevano scegliere l'interfaccia di rete appropriata in base all'indirizzo IP, alla subnet dell'interfaccia, al nome DNS (Domain Name System) associato all'interfaccia, all'indirizzo MAC di una scheda di interfaccia di rete, a un nome di rete wireless o ad altre informazioni di rete. NLA attenua questo problema fornendo un'interfaccia standard per l'enumerazione delle informazioni sugli allegati di rete logica, la correlazione con le informazioni sull'interfaccia di rete fisica e quindi la notifica quando le informazioni restituite in precedenza vengono invalidate.

NLA fornisce le informazioni seguenti sul percorso di rete:

<dl> <dt>

<span id="Logical_Network_Identity"></span><span id="logical_network_identity"></span><span id="LOGICAL_NETWORK_IDENTITY"></span>Identità di rete logica
</dt> <dd>

NLA tenta prima di tutto di identificare una rete logica in base al nome di dominio DNS. Se una rete logica non ha un nome di dominio, NLA identifica la rete dalle informazioni statiche personalizzate archiviate nel Registro di sistema e infine dal relativo indirizzo subnet.

</dd> <dt>

<span id="Logical_Network_Interfaces"></span><span id="logical_network_interfaces"></span><span id="LOGICAL_NETWORK_INTERFACES"></span>Interfacce di rete logica
</dt> <dd>

Per ogni rete a cui è collegato un computer, NLA fornisce un *adapterName* che identifica in modo univoco un'interfaccia fisica, ad esempio una scheda di interfaccia di rete, o un'interfaccia logica, ad esempio una connessione RAS. AdapterName può quindi essere usato con le funzioni disponibili nell'API helper IP per ottenere altre caratteristiche dell'interfaccia.

</dd> </dl>

NLA implementa la rete logica come classe di servizio, con un GUID e le proprietà della classe associati. Ogni rete logica per cui NLA restituisce informazioni è un'istanza di tale classe di servizio.

 

 



