---
description: Network Monitor offre tre funzioni per la selezione di una scheda di interfaccia di rete (NIC). Queste funzioni offrono tre modi per enumerare un set di schede di interfaccia di rete e selezionare quella che si vuole usare. Nella tabella seguente sono elencate queste funzioni.
ms.assetid: fbf319bb-4e24-46e3-81bc-d407b26220fb
title: Selezione di una scheda di interfaccia di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f93341bb169f2672579ac6764186925b7190f1ac52c698e2426e1c20d3e854
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074491"
---
# <a name="selecting-a-network-interface-card"></a>Selezione di una scheda di interfaccia di rete

Network Monitor offre tre funzioni per la selezione di una scheda di interfaccia di rete (NIC). Queste funzioni offrono tre modi per enumerare un set di schede di interfaccia di rete e selezionare quella che si vuole usare. Nella tabella seguente sono elencate queste funzioni.



| Funzione                                                 | Descrizione                                                                                                                                  |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetNPPBlobFromUI**](getnppblobfromui.md)             | Usa l'interfaccia Network Monitor per visualizzare le schede di interfaccia di rete registrate e restituisce il BLOB NPP che rappresenta la scheda di interfaccia di rete a cui si è interessati.           |
| [**GetNPPBlobTable**](getnppblobtable.md)               | Restituisce una tabella BLOB. L'applicazione deve enumerare la tabella e selezionare un BLOB NPP.                                                       |
| [**SelectNPPBlobFromTable**](selectnppblobfromtable.md) | Usa l Network Monitor per visualizzare i BLOB NPP forniti e restituisce il BLOB NPP che rappresenta la scheda di interfaccia di rete a cui si è interessati. |



 

Ogni scheda di interfaccia di rete è rappresentata da un BLOB (Binary Large Object) NPP. Queste funzioni possono restituire un singolo BLOB NPP da quelli registrati nel computer, un singolo BLOB NPP da una tabella BLOB NPP fornita o una tabella di BLOB NPP che il chiamante deve quindi usare per selezionare un BLOB specifico. Nei primi due casi, quando si esegue la selezione dalle schede di interfaccia di rete registrate o da una tabella BLOB NPP fornita, l'interfaccia utente di Network Monitor visualizza le schede di interfaccia di rete che è possibile selezionare.

> [!Note]  
> Network Monitor usa una funzionalità denominata Ricerca NPP per enumerare le schede di interfaccia di rete registrate nel computer locale. Il Finder NPP è un componente di Npptools.dll.

 



| Per informazioni su                            | Vedere                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Selezione di una scheda di interfaccia di rete registrata nel computer locale | [Selezione di una scheda di interfaccia di rete registrata](selecting-a-registered-nic.md)                                         |
| Selezione di una scheda di interfaccia di rete da una tabella BLOB NPP fornita   | [Selezione di una scheda di interfaccia di rete da una tabella BLOB NPP fornita](selecting-a-nic-from-a-supplied-npp-blob-table.md) |
| Recupero di una tabella BLOB NPP                     | [Selezione di una scheda di interfaccia di rete da una tabella BLOB NPP restituita](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



