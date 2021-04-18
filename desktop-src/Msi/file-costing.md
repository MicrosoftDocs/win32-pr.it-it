---
description: Il costo è il processo di determinazione dei requisiti di spazio totale su disco per un'installazione.
ms.assetid: 53ebb532-9eb3-46b7-9dcc-f593bfd25c60
title: Costo file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55a4e6221775c2b9ecc429bd32f136e519a2b63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309477"
---
# <a name="file-costing"></a>Costo file

Il costo è il processo di determinazione dei requisiti di spazio totale su disco per un'installazione. Gli elementi calcolati nel processo di determinazione dei costi dei file includono la quantità di spazio su disco in cui vengono installati o rimossi i file, nonché la quantità di spazio su disco occupata dalle voci del registro di sistema, dai collegamenti e da altri file esterni. I file esistenti pianificati per la sovrascrittura vengono calcolati anche nei totali dei costi del disco.

I costi totali vengono accumulati per singolo[componente](components-and-features.md) e sono costituiti da tre parti separate, ovvero costi locali, costi di origine e costi di rimozione. Queste parti corrispondono al costo del disco sostenuto se il componente viene installato localmente, installato per l'esecuzione dal supporto di origine o rimosso.

Tutti i calcoli che comportano il costo dell'installazione dei file dipendono dal volume del disco in cui il file deve essere installato o rimosso. Ogni volta che viene modificata la directory associata a un componente, è necessario ricalcolare i costi dei file di installazione controllati da tale componente. Poiché, ad esempio, una modifica alla directory potrebbe implicare una modifica del volume, è necessario ricalcolare le dimensioni dei file in cluster. Inoltre, è necessario controllare la nuova directory per determinare se è necessario prendere in considerazione tutti i file esistenti che possono essere sovrascritti.

Dopo la chiamata dell'azione [CostInitialize](costinitialize-action.md) , è necessario chiamare l'azione [filecost](filecost-action.md) . L'azione CostInitialize Inizializza le routine interne del programma di installazione che calcolano dinamicamente i costi del disco necessari per le azioni di installazione standard. A questo punto non vengono eseguiti altri calcoli di costo dinamico.

Successivamente, è necessario chiamare l'azione [CostFinalize secondo](costfinalize-action.md) . Questa azione consente di finalizzare tutti i calcoli sui costi e rende disponibili i dati relativi ai costi tramite la tabella dei [componenti](component-table.md) .

Al termine dell'esecuzione dell'azione [CostFinalize secondo](costfinalize-action.md) , la tabella dei [componenti](component-table.md) è stata inizializzata completamente e una sequenza di finestra di dialogo dell'interfaccia utente contenente un controllo [SelectionTree](selectiontree-control.md) può essere avviata, se necessario. Le finestre di dialogo dell'interfaccia utente possono offrire l'opzione per modificare lo stato di selezione o la directory di destinazione di qualsiasi funzionalità della tabella delle [funzionalità](feature-table.md) . Il processo è simile quando lo stato di selezione di un componente viene modificato; Tuttavia, in questo caso, il costo dinamico del componente modificato viene ricalcolato.

Una volta che l'utente ha completato la selezione delle funzionalità nell'interfaccia utente, deve essere chiamata l'azione [InstallValidate](installvalidate-action.md) . Questa azione verifica che tutti i volumi a cui è stato attribuito il costo dispongano di spazio sufficiente per l'installazione.

 

 



