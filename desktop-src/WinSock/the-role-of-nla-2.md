---
description: Il provider di servizi di riconoscimento del percorso di rete è essenziale per i computer o i dispositivi che possono spostarsi tra reti diverse e per selezionare configurazioni ottimali quando sono disponibili più di uno.
ms.assetid: 307f384d-e59a-4fc5-8f6a-ed81a102df60
title: Ruolo di NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28034d0d08353b3e794b5a30a6900e24d214e977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226957"
---
# <a name="the-role-of-nla"></a>Ruolo di NLA

Il provider di servizi di riconoscimento del percorso di rete è essenziale per i computer o i dispositivi che possono spostarsi tra reti diverse e per selezionare configurazioni ottimali quando sono disponibili più di uno. Ad esempio, un computer wireless che effettua il roaming tra reti fisiche può utilizzare NLA per determinare la configurazione corretta in base alle informazioni sulla connessione di rete disponibile. NLA si rivela utile anche quando un computer multihomed dispone di una connessione fisica a una rete, mentre è connessa anche a un'altra rete tramite una connessione remota o un tunnel.

In passato, gli sviluppatori dovevano ottenere informazioni su un'interfaccia di rete logica e quindi prendere decisioni sulla connettività di rete, in base a una grande quantità di informazioni di rete diversi. In questi casi, gli sviluppatori devono scegliere l'interfaccia di rete appropriata in base all'indirizzo IP, alla subnet dell'interfaccia, al nome del Domain Name System (DNS) associato all'interfaccia, all'indirizzo MAC di una scheda di interfaccia di rete, a un nome di rete wireless o ad altre informazioni sulla rete. NLA attenua questo problema fornendo un'interfaccia standard per l'enumerazione delle informazioni sugli allegati di rete logica, la correlazione con le informazioni sull'interfaccia di rete fisica e quindi la notifica quando le informazioni restituite in precedenza vengono invalidate.

NLA fornisce le seguenti informazioni sul percorso di rete:

<dl> <dt>

<span id="Logical_Network_Identity"></span><span id="logical_network_identity"></span><span id="LOGICAL_NETWORK_IDENTITY"></span>Identità rete logica
</dt> <dd>

NLA tenta innanzitutto di identificare una rete logica in base al nome di dominio DNS. Se una rete logica non ha un nome di dominio, NLA identifica la rete da informazioni statiche personalizzate archiviate nel registro di sistema e infine dall'indirizzo della subnet.

</dd> <dt>

<span id="Logical_Network_Interfaces"></span><span id="logical_network_interfaces"></span><span id="LOGICAL_NETWORK_INTERFACES"></span>Interfacce di rete logiche
</dt> <dd>

Per ogni rete a cui è collegato un computer, NLA fornisce un *AdapterName* che identifica in modo univoco un'interfaccia fisica, ad esempio una NIC, oppure un'interfaccia logica quale una connessione RAS. AdapterName può quindi essere usato con le funzioni disponibili nell'API helper IP per ottenere ulteriori caratteristiche di interfaccia.

</dd> </dl>

NLA implementa la rete logica come classe del servizio, con le proprietà e il GUID della classe associati. Ogni rete logica per cui NLA restituisce informazioni è un'istanza di tale classe di servizio.

 

 



