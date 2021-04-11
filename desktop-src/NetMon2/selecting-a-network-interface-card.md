---
description: Network Monitor offre tre funzioni per la selezione di una scheda di interfaccia di rete (NIC). Queste funzioni forniscono tre modi per enumerare un set di schede di rete e selezionare quello che si vuole usare. Nella tabella seguente sono elencate queste funzioni.
ms.assetid: fbf319bb-4e24-46e3-81bc-d407b26220fb
title: Selezione di una scheda di interfaccia di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8315a97cc8457d86614fc25c87c39b1b9794c7fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131191"
---
# <a name="selecting-a-network-interface-card"></a>Selezione di una scheda di interfaccia di rete

Network Monitor offre tre funzioni per la selezione di una scheda di interfaccia di rete (NIC). Queste funzioni forniscono tre modi per enumerare un set di schede di rete e selezionare quello che si vuole usare. Nella tabella seguente sono elencate queste funzioni.



| Funzione                                                 | Descrizione                                                                                                                                  |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetNPPBlobFromUI**](getnppblobfromui.md)             | Usa l'interfaccia utente di Network Monitor per visualizzare le schede NIC registrate e restituisce il BLOB di NPP che rappresenta la scheda di interfaccia di rete a cui si è interessati.           |
| [**GetNPPBlobTable**](getnppblobtable.md)               | Restituisce una tabella BLOB. L'applicazione deve enumerare la tabella e selezionare un BLOB di NPP.                                                       |
| [**SelectNPPBlobFromTable**](selectnppblobfromtable.md) | Usa l'interfaccia Network Monitor per visualizzare i BLOB NPP specificati e restituisce il BLOB di NPP che rappresenta la scheda di interfaccia di rete a cui si è interessati. |



 

Ogni scheda di interfaccia di rete è rappresentata da un BLOB (Binary Large Object) di NPP. Queste funzioni possono restituire un singolo BLOB NPP da quelli registrati nel computer, un singolo BLOB NPP da una tabella BLOB NPP specificata o una tabella di BLOB NPP che il chiamante deve usare per selezionare un BLOB specifico. Nei primi due casi, quando si selezionano le schede NIC registrate o da una tabella BLOB NPP specificata, l'interfaccia utente di Network Monitor Visualizza le schede di interfaccia di rete che è possibile selezionare.

> [!Note]  
> Network Monitor usa una funzionalità denominata ricercatore NPP per enumerare le schede di rete registrate nel computer locale. Il Finder di NPP è un componente di Npptools.dll.

 



| Per informazioni su                            | Vedere                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Selezione di una scheda di interfaccia di rete registrata nel computer locale | [Selezione di una scheda di interfaccia di rete registrata](selecting-a-registered-nic.md)                                         |
| Selezione di una scheda di interfaccia di rete da una tabella BLOB NPP specificata   | [Selezione di una scheda di interfaccia di rete da una tabella BLOB NPP specificata](selecting-a-nic-from-a-supplied-npp-blob-table.md) |
| Recupero di una tabella BLOB di NPP                     | [Selezione di una scheda di interfaccia di rete da una tabella BLOB NPP restituita](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



