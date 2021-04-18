---
description: Per selezionare una delle schede di rete registrate nel computer locale, chiamare la funzione GetNPPBlobFromUI.
ms.assetid: ca1fb07f-7eee-419f-b25d-49718d02fc7d
title: Selezione di una scheda di interfaccia di rete registrata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b7047d5bbb46797210e18782c672cfd81b9cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310490"
---
# <a name="selecting-a-registered-nic"></a>Selezione di una scheda di interfaccia di rete registrata

Per selezionare una delle schede di rete registrate nel computer locale, chiamare la funzione [**GetNPPBlobFromUI**](getnppblobfromui.md) . Questa funzione usa l'interfaccia utente di Network Monitor per visualizzare le schede di interfaccia di rete registrate e restituisce il BLOB di NPP che rappresenta la scheda di interfaccia di rete selezionata. È possibile visualizzare tutte le schede di rete registrate nel computer locale o un set più piccolo di schede di rete filtrate. Per filtrare le NIC visualizzate, fornire un [*BLOB di filtro*](f.md) quando viene effettuata la chiamata.

> [!Note]  
> Quando viene chiamata la funzione [**GetNPPBlobFromUI**](getnppblobfromui.md) , il [*Finder di NPP*](n.md) comunica con le DLL di NPP per ottenere le strutture BLOB di NPP che rappresentano le schede NIC registrate. Per ulteriori informazioni e per una procedura su come utilizzare direttamente l'interfaccia utente di Network Monitor, vedere l'argomento "selezionare una rete nella finestra di dialogo" nella Guida in linea di Network Monitor.

 

Quando si chiama la funzione [**GetNPPBlobFromUI**](getnppblobfromui.md) , viene visualizzata la finestra **di dialogo selezionare una rete** . È possibile visualizzare i dettagli di centrali registrati nel computer locale. Queste informazioni includono sia centrali locale che centrali remoto. Nella finestra di dialogo è possibile selezionare una scheda di interfaccia di rete specifica e visualizzare i dettagli della struttura del BLOB di NPP associata.

Nella figura seguente sono illustrate le impostazioni tipiche di una NPP di tipo NDIS fornita da Network Monitor.

![impostazioni tipiche di una NPP di tipo NDIS fornita da Network Monitor](images/networkdb.png)

Nella tabella seguente sono elencati gli argomenti che descrivono ogni metodo di selezione NIC.



| Per informazioni su                                                                          | Vedere                                                                                                  |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Come specificare un filtro che limita le NIC visualizzate nella finestra di dialogo **Seleziona rete** . | [Specifica di un BLOB di filtro](specifying-a-filter-blob.md)                                             |
| Come selezionare una scheda di interfaccia di rete chiamando la funzione [**GetNPPBlobFromUI**](getnppblobfromui.md) .      | [Selezione di una scheda di interfaccia di rete con GetNPPBlobFromUI](getnppblobfromui.md)                                       |
| Come selezionare una scheda di interfaccia di rete da una tabella BLOB NPP specificata.                                            | [Selezione di una scheda di interfaccia di rete da una tabella BLOB NPP specificata](selecting-a-nic-from-a-supplied-npp-blob-table.md) |



 

 

 



